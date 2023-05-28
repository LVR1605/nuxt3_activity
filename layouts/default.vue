<template>
    <div class="flex justify-center w-auto font-roboto text-3xl bg-black">
        <ul class="flex justify-center items-center">
            <li class="text-white m-5 hover:text-red-500 transition-colors duration-500"> <nuxt-link to="/">Home</nuxt-link></li>
            <li class="text-white m-5 hover:text-red-500 transition-colors duration-500"> <nuxt-link to="/products">Products</nuxt-link></li>
        </ul>
        <div>
            <slot />
        </div>    
    </div>
    <div class="flex justify-center items-center h-screen text-5xl">
        <p>WELCOME TO FAKESTOREAPI</p>
    </div>
</template>
<style scoped>
</style>