<template>
    <div>
<!-- <h2>Products</h2>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Neque quo laudantium facere ad dolorem sed, molestiae quia voluptatem fugit. Sequi beatae eos nesciunt esse id neque ipsam, voluptate inventore voluptatibus.</p> -->
<div class="grid grid-cols-4 gap-5">
    <div v-for="p in products">
        <!-- <NuxtLink :to="`/products/${p.id}`">{{p.title }}</NuxtLink> -->
        <ProductCard  :product="p"/>

    </div>
</div>
    </div>
</template>

<script setup>
definePageMeta({
    layout:'products'

})

//fetch the products
const {data:products}=await useFetch('https://fakestoreapi.com/products/') 

useHead({
    title:'Nuxt Dojo | Merch',
    meta:[
        {
            name:'description', content:'Nuxt 3 Merch'
        }
    ]
})

</script>

<style lang="scss" scoped>

</style>