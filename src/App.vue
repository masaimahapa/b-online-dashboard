<template>
<div class="container-fluid">
  <div class="row">
    <HeaderItem 
    class="pt-2"
    :toggleSidebar="toggleSidebar"/>
  </div>
  <hr />
  
  <div class="row">
    <div class="col-6 col-md-2">
      <SideNav 
      class="mt-md-2"
      :showSidebar="showSidebar"
      :currentRouteName="currentRouteName"
      :toggleSidebar="toggleSidebar"
      />
    </div>
    
  <div :class="showSidebar ? 'col-10 offset-2': 'col-12'" class="offset-md-3 col-md-9">
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
    },
    toggleSidebar(){
      this.showSidebar = !this.showSidebar
    }
  },
  computed: {
    currentRouteName(){
      return this.$route.name;
    }
  },
  data () {
    return {
      users: userData,
      currentUser: userData[0],
      showSidebar:false
    }
  }
}
</script>
