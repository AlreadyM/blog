<template>
    <div>
        <!--<ComponentName or html/>-->
        <NuxtLink class="navlink" to="/">Home</NuxtLink> 
        <NuxtLink class="navlink" to="/nuxt">Nuxt</NuxtLink> 
        <NuxtLink class="navlink" to="/exchange">Exchange</NuxtLink> 
        <NuxtLink class="navlink" to="/vue">Vue</NuxtLink> 
    </div>
</template>

<script setup> // use lang='ts' set the script with typescript
    // import  {ref} from 'vue';
    // import { storeToRefs } from 'pinia';
    
</script>

<style scoped>
    .navlink{
        display: inline-block;
        padding-right: 20px;
    }
</style>