<template>
    <h1>Billing</h1>
    <p>Overview of your accounts</p>
    <UserCard 
    v-for="(account, index) in users"
    :user="account"
    :key="index"/>
</template>

<script>
import UserCard from '../components/UserCard.vue'

export default {
    props:['users'],
    components:{
        UserCard
    }
}
</script>