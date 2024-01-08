<script setup>
import {RouterLink, RouterView} from 'vue-router'


</script>

<template>
  <!--
  <header class="px-7 py-5 w-full min-h-10  flex justify-between items-center gap-x-64 shadow-lg rounded-3xl	">
    <div>
      <h3>Léo</h3>
    </div>
    <nav class="w-full flex justify-evenly z-50">
      <a href="#about">À propos</a>
      <a href="#realisation">Réalisation</a>
      <a href="#competence">Compétence</a>
      <a href="#contact">Contact</a>
    </nav>
    <div>
      <h3>Language</h3>
    </div>
  </header>
  -->

  <RouterView/>
</template>

<style>
* {
  box-sizing: border-box;
  scroll-behavior: smooth;
}

.fade-in {
  opacity: 0;
  transition: opacity 0.6s ease-in-out;
}

.fade-in.is-visible {
  opacity: 1;
}

</style>