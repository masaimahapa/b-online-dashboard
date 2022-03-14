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
                <div class="col-12 col-md-5 p-3 light-grey rounded ms-md-4 me-md-4">
                    <h6>Current balance</h6>
                    <h3> £{{currentUser.balance}}</h3>
                    <div class="row">
                        <div class="col-2">
                            <BIconLockFill />
                        </div>
                        <div class="col-10">
                            <p>This is a secure 256-bit SSL encrypted payment. You're safe.</p>
                        </div>
                        <button class="btn col-5 text-white ms-2 custom-button">
                            Pay Now
                        </button>
                    </div>
                </div>
                <div class="col-12 col-md-5 p-3 mt-2 mt-md-0 light-grey">
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
                    <button class="btn custom-button col-8 text-white ms-2">
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

