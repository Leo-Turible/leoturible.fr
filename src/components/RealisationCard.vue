<script setup>
import { defineProps } from 'vue'

defineProps({
  title: String,
  description: String,
  image: String
})
</script>

<template>
  <div class="card-realisation snap-center flex flex-col items-center justify-start h-auto max-w-72 w-full min-h-96 bg-slate-300 p-1.5 rounded-xl flex-shrink-0">
    <div class="card-realisation__img max-w-full">
      <img :src="image" alt="" class="rounded">
    </div>
    <div class="card-realisation__content ">
      <h3 class="card-realisation__title text-center">{{ title }}</h3>
      <p class="card-realisation__description text-justify">{{ description }}</p>
    </div>
  </div>
</template>

<style scoped>

</style>