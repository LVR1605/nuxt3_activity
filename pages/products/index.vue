<template>
    <div>
        <ul class="navbar">
            <li class="nav-item"> <nuxt-link to="/">Home</nuxt-link></li>
            <li class="nav-item"> <nuxt-link to="/products">Products</nuxt-link></li>
          </ul>        
    </div>
    <div class="grid-container">
        <div class="grid-item" v-for="p in products"><nuxt-link :to="`/products/${p.id}}`">{{ p.title }}</nuxt-link></div>
        <div class="grid-item"></div>
        <div class="grid-item"></div>
    </div>
</template>

<script setup>
    definePageMeta(
        {
            layout: 'products'
        }
    )

    const { data: products } = await useFetch('https://fakestoreapi.com/products')
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

    .grid-container {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-gap: 20px;
      }
  
      .grid-item {
        padding: 50px;
        text-align: center;
      }
</style>