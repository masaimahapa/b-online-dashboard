<template>
   <div class="row flex justify-content-between">
       <div class="col-9">
           <div class="row flex justify-content-between">
               <div class="col-3">
                   <span class="fs-4">bOnline</span>
               </div>
               <div class="col-2">
                <BIconBell class="icon"/>
            </div>
               
           </div>
            
       </div>
       

        <div class="col-3">
            <div class="row">
                <div class="col-3">
                    <img 
                    src="../assets/masai.jpg"
                    class="rounded-circle img-fluid"
                    alt="profile picture"

                    />
                </div>
                <div class="col-8">
                    <span class="fs-5">First LastName</span>
                    <p>firstlastname@bonline.com</p>
                    
                </div>
                <div class="col-1">
                    <BIconChevronDown class="mt-4"/>
                </div>
            </div>
            
        </div>
    </div>
</template>

<style scoped>
    .header {
        position: fixed;
        top: 0;
        left:0;
        right: 0;
        margin: 20px;
    }
</style>

<script>
import { BIconBell, BIconChevronDown} from 'bootstrap-icons-vue'

export default {
    components: {
        BIconBell,
        BIconChevronDown
    }
}
</script>