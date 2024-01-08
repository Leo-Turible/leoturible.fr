<script setup>
import {defineProps, ref, onMounted} from 'vue'
import RealisationCard from './RealisationCard.vue'

defineProps({
  cards: {
    type: Array,
    required: true
  }
})

let slider = ref(null);

onMounted(() => {
  slider.value = document.querySelector('#slider');
});

const scrollLeft = () => {
  const cardWidth = slider.value.querySelector('.card-realisation').offsetWidth;
  slider.value.scrollLeft -= cardWidth;
};

const scrollRight = () => {
  const cardWidth = slider.value.querySelector('.card-realisation').offsetWidth;
  slider.value.scrollLeft += cardWidth;
};
</script>

<template>
  <div class="relative flex items-center justify-center">
    <button @click="scrollLeft" class="absolute left-36 z-50"><</button>
    <button @click="scrollRight" class="absolute right-36 z-50">></button>

    <div id="slider"
         class="flex flex-nowrap items-start justify-start gap-16 w-[80%] overflow-x-scroll snap-x snap-mandatory">

      <div class="w-1/2 flex-shrink-0"></div>

      <RealisationCard
          v-for="card in cards"
          :key="card.id"
          :title="card.title"
          :description="card.description"
          :image="card.image"
          :url="card.url"
      />

      <div class="w-1/2 flex-shrink-0"></div>
    </div>
  </div>
</template>

<style scoped>
#slider::-webkit-scrollbar {
  display: none;
}

#slider {
  scrollbar-width: none;
}

button {
  background-color: #ffffff;
  border: none;
  border-radius: 50%;
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5rem;
  color: #000000;
  cursor: pointer;
  opacity: 0.7;
  transition: opacity 0.3s ease;
}

button:hover {
  opacity: 1;
}

button:active {
  transform: scale(0.95);
}
</style>