<template>
    <div class="card">
        <div class="card-body">
            <h5 class="card-title">
                Payment details
            </h5>
            <p class="card-subtitle">
                View details of your next invoice and payment method
            </p>
            <hr/>
            <h6>Next invoice: {{formatDate(currentUser.next_invoice_date)}}</h6>

            <div class="row">
                <div class="col-5 p-3 light-grey rounded ms-4 me-4">
                    <h6>Current balance</h6>
                    <h3> £{{currentUser.balance}}</h3>
                    <div class="row">
                        <div class="col-2">
                            <BIconLockFill />
                        </div>
                        <div class="col-10">
                            <p>This is a secure 256-bit SSL encrypted payment. You're safe.</p>
                        </div>
                        <button class="btn bg-primary col-5 text-white ms-2">
                            Pay Now
                        </button>
                    </div>
                </div>
                <div class="col-5 p-3 light-grey">
                    <h6>Payment method 
                        <span class="badge badge-secondary text-dark">Annual</span>
                    </h6>
                    <div class="row">
                        <div class="col-2">
                        <BIconLightbulbFill />
                    </div>
                    <div class="col-10">
                        <p>
                            Guide: To manage your payments more easily, we recommend switching to Direct Debit.
                        </p>
                    </div>
                    <button class="btn col-8 bg-primary text-white ms-2">
                            Switch to Direct Debit
                        </button>
                    </div>
                    
                </div>
               
            </div>
        </div>
        
    </div>
</template>



<script>
import { BIconLockFill, BIconLightbulbFill} from 'bootstrap-icons-vue'


export default {
    props:['currentUser', 'formatDate'],
    components: {
        BIconLockFill,
        BIconLightbulbFill
    },
}
</script>

