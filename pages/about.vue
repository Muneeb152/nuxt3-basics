<template>
    <div>
<h2>About</h2>
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Neque quo laudantium facere ad dolorem sed, molestiae quia voluptatem fugit. Sequi beatae eos nesciunt esse id neque ipsam, voluptate inventore voluptatibus.</p>
      <div>
        {{ data }}
      </div>
    </div>
</template>

<script setup>
 //const {data}=await useFetch('/api/ninja')
const {data}=await useFetch('/api/currency/GBP')
</script>

<style lang="scss" scoped>

</style>