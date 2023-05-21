<template>
    <div>
        <ul class="navbar">
            <li class="nav-item"> <nuxt-link to="/">Home</nuxt-link></li>
            <li class="nav-item"> <nuxt-link to="/products">Products</nuxt-link></li>
          </ul>        
    </div>
    <div class="toCenter">
        <div class="header">WELCOME TO FAKESTOREAPI</div>
    </div>
</template>

<script setup>

</script>

<style  scoped>
    .toCenter {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        margin: 0;
    }
    .header {
        font-size: 36px;
        text-align: center;
    }

    ul {
        display: flex;
        justify-content: center;
        font-size: larger;
    }
    ul.navbar {
        list-style-type: none;
        margin: 0;
        padding: 0;
        overflow: hidden;
        background-color: #333;
    }

    li.nav-item {
        float: left;
    }

    li.nav-item a {
        display: block;
        color: white;
        text-align: center;
        padding: 14px 16px;
        text-decoration: none;
    }

    li.nav-item a:hover {
        background-color: #111;
    }
</style>