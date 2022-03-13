<template>
    <div class="card" @click="selectAccount(user.account_id)">
        <div class="container">
            <h4>{{user.first_name}} <span :class="statusClass">{{user.account_status}}</span></h4>
            <span>Account ID : {{user.account_id}}</span>
        </div>
    </div>
</template>

<script>

export default {
    props: ['user', 'selectAccount'],
    computed: {
        statusClass: function(){
                const status = this.user.account_status.toLowerCase()
                if (status==='live'){
                    return 'active-badge'
                } else if(status==="suspended"){
                    return 'suspended-badge'
                }
                else {
                    return "inactive-badge"
                }
            
        }
    }
}
</script>

<style scoped>
  .active-badge{
    color: #19D5B2;
    background-color: #e4fdf9;
    font-size: 12px;
  }
  .suspended-badge{
    color: rgb(255, 136, 0);
    background-color: rgb(248, 240, 226);
    font-size: 12px;
  }
    .inactive-badge{
    color: #ee1009;
    background-color: #f5eeeb;
    font-size: 12px;
  }

    .card {
        box-shadow: 0 2px 4px 0;
    }

    .card:hover {
        box-shadow: 0 4px 4px 0;
    }

    .container {
        padding: 2px;
    }
</style>