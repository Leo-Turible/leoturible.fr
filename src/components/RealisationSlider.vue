<script setup>
import { defineProps } from 'vue'
import RealisationCard from './RealisationCard.vue'

defineProps({
  cards: {
    type: Array,
    required: true
  }
})
</script>

<template>
  <div id="slider"
       class="flex flex-nowrap items-start justify-start gap-16 w-[80%] overflow-x-scroll snap-x snap-mandatory">
    <div class="w-1/2 flex-shrink-0"></div>

    <RealisationCard
        v-for="card in cards"
        :key="card.id"
        :title="card.title"
        :description="card.description"
        :image="card.image"
    />

    <div class="w-1/2 flex-shrink-0"></div>
  </div>
</template>

<style scoped>
#slider::-webkit-scrollbar {
  display: none;
}

#slider {
  scrollbar-width: none;
}
</style>