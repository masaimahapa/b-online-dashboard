<template>
    <aside class="sidenav">
        <ul>
            <li>
                <router-link to="/">
                    <span>Home</span>
                </router-link>
            </li>
            <li>
                <router-link to="/billing">
                    <span>Billing</span>
                </router-link>
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

    a:hover {
        background-color: #1F8CEB;
    }

    .sidenav {
        height: 100%;
        width: 20%;
        position: fixed;
        left: 0;
    }
</style>