<template>
    <div class="flex justify-center font-roboto text-3xl bg-black">
        <ul class="flex">
            <li class="text-white m-5 hover:text-red-500 transition-colors duration-500"> <nuxt-link to="/">Home</nuxt-link></li>
            <li class="text-white m-5 hover:text-red-500 transition-colors duration-500"> <nuxt-link to="/products">Products</nuxt-link></li>
          </ul>        
    </div>
    <div class="m-28">    
        <p class="text-5xl">{{ product.title }}</p>
        <p class="text-3xl">{{ product.price }}</p>
        <p class="text-3xl">{{ product.id }}</p>
    </div>
</template>

<script setup>
    const{ id } =  useRoute().params
    const uri = 'https://fakestoreapi.com/products/' + id

    const { data: product } = await useFetch(uri, { key: id } )

    definePageMeta
    (
        {
            layout: 'products'
        }
    )
</script>

<style scoped>

</style>