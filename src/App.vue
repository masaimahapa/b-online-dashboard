<template>
<div class="container-fluid">
  <div class="row">
    <HeaderItem class="py-2"/>
  </div>
  <hr />
  
  <div class="row">
    <div class="col-2">
      <SideNav class="mt-2"/>
    </div>
    
  <div class="col-10">
      <router-view 
      :users="users" 
      :selectAccount="selectAccount"
      :currentUser="currentUser"/>
  </div>
  </div>
  
</div>



</template>

<script>
import "bootstrap/dist/css/bootstrap.min.css"
import HeaderItem from './components/HeaderItem.vue'
import SideNav from './components/SideNav.vue'
import userData from './Data.json'


export default {
  name: 'App',
  components: {
    HeaderItem,
    SideNav
  },

  methods: {
    isUser(account, accountId){
      return account.account_id === accountId;
    },
     selectAccount(accountId) {
        this.currentUser = userData.find(each => this.isUser(each, accountId));
        console.log(accountId)
        console.log(this.currentUser); 
    }
  },
  data () {
    return {
      users: userData,
      currentUser: userData[0]
    }
  }
}
</script>






<style>
#app {
  color: #2c3e50;
}
 .light-grey {
        background-color: #eaeef3;
    }
      .icon {
        font-size: 30px;
    }


    .page {
        /* text-align: center; */
        /* margin-left:10%;
        margin-top: 50px; */
    }

</style>
