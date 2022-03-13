<template>
    <div class="card">
        <div class="card-body">
            <div class="card-title">
                <h5>My products</h5>
            </div>
            <div class="card-subtitle">
                <p>
                    All your products at a glance
                </p>
            </div>
            <hr />
            <div class="row p-2" v-for="(prod, index) in products" :key="index">
                {{prod.product_kind}} - {{prod.product_detail}}
                <hr/>
            </div>
        </div>
    </div>
    
</template>

<script>

export default {
    props: ['products']
}
</script>