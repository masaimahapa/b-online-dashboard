<template>
    <aside :class="showSidebar ? 'd-block': 'd-none' " class="sidenav d-md-block">
        <ul >
            <li>
                <div class="col-11 link-container p-2">
                     <router-link  class="col-12" to="/">
                    <BIconHouseDoor class="icon" /><span>Home</span>
                </router-link>
                </div>
               
            </li>
            <li>
                <div class="col-11 link-container p-2">
                    <router-link to="/billing">
                    <BIconCreditCard class="icon"/> <span>Billing</span>
                    </router-link>
                </div>
            </li>
        </ul>
    </aside>
</template>

<style scoped>

    ul {
        list-style: none;
    }
    a {
        color: black;
        text-decoration: none; 
    }

    .link-container:hover {
        background-color: #1F8CEB;
    }

    .sidenav {
        height: 100%;
        /* width: 15%; */
        /* position: fixed; */
        display: flex;
        flex-direction: column;
        border-right: 1px solid;
        border-color: #394455;
    }
</style>

<script>
import { BIconHouseDoor, BIconCreditCard } from 'bootstrap-icons-vue'

export default {
    props:['showSidebar'],
    components: {
        BIconHouseDoor, 
        BIconCreditCard
    }
}
</script>
