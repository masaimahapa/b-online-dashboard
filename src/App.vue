<template>
  <HeaderItem />
  <SideNav />
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <HelloWorld msg="Welcome to Your Vue.js App"/>

  <router-view :users="users"/>
</template>

<script>
import HeaderItem from './components/HeaderItem.vue'
import SideNav from './components/SideNav.vue'
import userData from './Data.json'

export default {
  name: 'App',
  components: {
    HeaderItem,
    SideNav
  },
  data () {
    return {
      users: userData
    }
  }
}
</script>






<style>
#app {
  text-align: center;
  color: #2c3e50;

}
</style>
