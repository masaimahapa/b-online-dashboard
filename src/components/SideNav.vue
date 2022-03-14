<template>
    <aside :class="showSidebar ? 'd-block bg-light col-6': 'd-none' " class="sidenav col-md-3 d-md-block">
        <ul >
            <li>
                <div :class="currentRouteName ==='home' ? 'blue-background': '' " class="col-11 link-container p-2">
                     <router-link @click="toggleSidebar"  class="col-12 text-dark" to="/">
                    <BIconHouseDoor class="icon" /><span>Home</span>
                </router-link>
                </div>
               
            </li>
            <li>
                <div  :class="currentRouteName ==='billing' ? 'blue-background': '' " class="col-11 link-container p-2">
                    <router-link @click="toggleSidebar" to="/billing" class="text-dark">
                    <BIconCreditCard  class="icon"/> 
                        <span>Billing</span>
                    </router-link>
                </div>
            </li>
        </ul>
    </aside>
</template>

<script>
import { BIconHouseDoor, BIconCreditCard } from 'bootstrap-icons-vue'

export default {
    props:['showSidebar', 'currentRouteName', 'toggleSidebar'],
    components: {
        BIconHouseDoor, 
        BIconCreditCard
    }
}
</script>
