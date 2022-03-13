<template>
    <main class="page"> 
    <h1>Billing</h1>
    <p>Overview of your accounts</p>
    <hr/>

    <div class="container-fluid light-grey">
        <div v-if="users.length">
        <div class="account-list row">
            
            <UserCard 
            class="card col-3 m-2"
            v-for="(account, index) in users"
            :user="account"
            :key="index"
            :selectAccount="selectAccount"
            />
        </div>
    </div>
    <hr/>
    <div class="row">
        <div class="col-8">
            <PaymentDetails
                :currentUser="currentUser"
                :formatDate="formatDate"
             />
        </div>
        <div class="col-4">
            <MyProducts
            :products="currentUser.products" />
        </div>
    </div>
    <div class="row mt-4">
        <BillingHistory
        
        :formatDate="formatDate" />
    </div>
   
    </div>

     
    </main>
</template>

<script>
import moment from 'moment'
import UserCard from '../components/UserCard.vue'
import PaymentDetails from '../components/PaymentDetails.vue'
import MyProducts from '../components/MyProducts.vue'
import BillingHistory from '../components/BillingHistory.vue'

export default {
    props:['users', 'selectAccount', 'currentUser'],
        methods:{
        formatDate(uglyDate){
            return moment(uglyDate).format("D MMM YYYY");
        }
    },

    components:{
        UserCard,
        PaymentDetails,
        MyProducts,
        BillingHistory
    }
}
</script>

<style scoped>
    /* .card {
        width: 130px;
        margin: 10px;
    }  */
    .account-list {
        display: inline-block;
        display: flex;
        justify-content:flex-start;
        

    }
</style>