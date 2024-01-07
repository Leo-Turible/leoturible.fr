<script setup>
import {RouterLink, RouterView} from 'vue-router'
</script>

<template>
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

  <RouterView/>
</template>

<style>
* {
  box-sizing: border-box;
  scroll-behavior: smooth;
}
/*
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}*/
</style>
