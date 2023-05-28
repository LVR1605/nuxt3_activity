<template>
    <div class="flex justify-center font-roboto text-3xl bg-black">
        <ul class="flex">
            <li class="text-white m-5 hover:text-red-500 transition-colors duration-500"> <nuxt-link to="/">Home</nuxt-link></li>
            <li class="text-white m-5 hover:text-red-500 transition-colors duration-500"> <nuxt-link to="/products">Products</nuxt-link></li>
          </ul>        
    </div>
    <div class="grid grid-cols-3 gap-5 text-2xl text-center">
        <div class="m-2 shadow hover:text-red-500 transition-colors duration-500" v-for="p in products">
            <nuxt-link :to="`/products/${p.id}`">{{ p.title }}</nuxt-link>
        </div>
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
</style>