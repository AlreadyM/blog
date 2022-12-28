<!-- <template>
    <div>
        <main class="prose">
            <ContentDoc path="/blog"/>
        </main>
    </div>
</template>

<script setup> // use lang='ts' set the script with typescript
    // import  {ref} from 'vue';
    // import { storeToRefs } from 'pinia';

</script> -->




<script setup>
const { path } = useRoute()

const { data } = await useAsyncData(`content-${path}`, () => {
  return queryContent().where({ _path: path }).findOne()
})
</script>

<template>
  <main class="prose text-left">
    <ContentRenderer v-if="data" :value="data" />
  </main>
</template>

<style scoped>

</style>