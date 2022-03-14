<template>
    <div :class="isTheCurrentUser?'border border-primary active-card':'' " class="card" @click="selectAccount(user.account_id)">
        <div class="container">
            <h4>{{user.first_name}} <span :class="statusClass" class="account-status">{{user.account_status}}</span></h4>
            <span>Account ID : {{user.account_id}}</span>
        </div>
    </div>
</template>

<script>

export default {
    props: ['user', 'selectAccount', 'isTheCurrentUser'],
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

