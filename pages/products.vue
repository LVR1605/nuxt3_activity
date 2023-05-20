<template>
    <div>
        <ul class="navbar">
            <li class="nav-item"><a href="">Home</a></li>
            <li class="nav-item"><a href="/products">Products</a></li>
          </ul>        
    </div>
</template>

<script setup>

</script>

<style  scoped>

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