<script setup>
import {defineProps, computed} from 'vue'

const props = defineProps({
  title: String,
  description: String,
  image: String,
  url: String,
  skills: Array
})

const imageName = computed(() => {
  // Extraire le nom du fichier sans l'extension
  return props.image ? props.image.split('/').pop().split('.')[0] : '';
});
</script>

<template>
  <div
      class="card-realisation snap-center flex flex-col items-center justify-start h-auto max-w-72 w-full min-h-96 bg-slate-50 rounded-xl flex-shrink-0 overflow-hidden shadow-2xl">
    <div class="card-realisation__img max-w-full">
      <img :src="image" :alt="`Image du site ${imageName}`" class="">
    </div>
    <div class="skills flex items-center justify-around w-full border-slate-900 border-y-2 py-1.5">
      <img v-for="skill in skills" :src="`/ico/${skill}.svg`" :alt="skill" key="skill" class="h-10">
    </div>
    <div class="card-realisation__content flex items-stretch justify-start flex-col h-full">
      <h3 class="card-realisation__title text-center text-3xl font-bold dark:text-white pt-2.5">
        {{ title }}</h3>
      <p class="card-realisation__description text-justify p-3.5 text-gray-500">{{ description }}</p>
      <a :href="url"
         class="card-realisation__discover-link self-center px-10 py-2.5 m-3.5 bg-indigo-500 text-white rounded-xl transition ease-in-out hover:bg-indigo-300 hover:scale-110 mt-auto">Découvrir</a>
    </div>
  </div>
</template>

<style scoped>

</style>