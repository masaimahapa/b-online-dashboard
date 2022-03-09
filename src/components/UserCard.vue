<template>
    <div class="card">
        <div class="container">
            <h4>{{user.first_name}}</h4>
            <span>Account ID : {{user.account_id}}</span>
        </div>
    </div>
</template>

<script>

export default {
    props: ['user']
}
</script>

<style scoped>
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