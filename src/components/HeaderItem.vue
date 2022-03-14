<template>
   <div class="row flex justify-content-between">
       
       <div class="col-12 col-md-8">
           <div class="row flex justify-content-between">
               <div class="col-md-3 col-6">
                   <button class="btn" @click="toggleSidebar">
                       <BIconList class="d-inline d-md-none icon me-2 me-md-0" />
                   </button>    
                   <span class="fs-4">bOnline</span>
               </div>
               <div class="col-2">
                <BIconBell class="icon"/>
            </div>
               
           </div>
            
       </div>
       

        <div class="col-12 col-md-4">
            <div class="row">
                <div class="col-3 col-md-3">
                    <img 
                    src="../assets/masai.jpg"
                    class="rounded-circle img-fluid"
                    alt="profile picture"

                    />
                </div>
                <div class="col-8 col-md-7">
                    <span class="fs-6 fs-md-5">First LastName</span>
                    <p>firstlastname@bonline.com</p>
                    
                </div>
                <div class="col-1 col-md-1">
                    <BIconChevronDown class="mt-lg-4"/>
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
import { BIconBell, BIconChevronDown, BIconList} from 'bootstrap-icons-vue'

export default {
    props:['toggleSidebar'],
    components: {
        BIconBell,
        BIconChevronDown,
        BIconList
    }
}
</script>