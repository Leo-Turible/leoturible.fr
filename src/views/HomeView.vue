<script setup>
import RealisationSlider from '../components/RealisationSlider.vue'
import SkillsComponent from '../components/SkillsComponent.vue'
import ContactForm from '../components/ContactForm.vue'
import {onMounted, nextTick} from 'vue';

onMounted(() => {
  console.log('onMounted called');
  nextTick(() => {
    console.log('nextTick called');
    const elements = document.querySelectorAll('.fade-in');

    const observer = new IntersectionObserver((entries) => {
      console.log('IntersectionObserver callback called');
      entries.forEach(entry => {
        console.log('IntersectionObserver entry:', entry);
        if (entry.isIntersecting) {
          entry.target.classList.add('is-visible');
        } else {
          entry.target.classList.remove('is-visible');
        }
      });
    }, {
      threshold: 0.5
    });

    elements.forEach(element => {
      observer.observe(element);
    });
  });
});
const cards = [
  {
    id: 1,
    title: 'Fallout',
    description: 'Ce site a été conçu sur le thème de l\'univers de Fallout. Il a été réalisé en HTML, CSS et JavaScript dans le cadre d\'un projet en cours. J\'y ai fait mes premiers pas avec JavaScript afin d\'implémenter un système de musique que l\'on peut mute/unmute et afin de permettre à l\'utilisateur de savoir sur quelle page il se trouve grâce à une classe active dans le header.html.',
    image: '/fallout.webp',
    url: 'https://fallout.leoturible.fr'
  },
  {
    id: 2,
    title: 'Zelda',
    description: 'Ce site a été conçu sur le thème de l\'univers de Zelda. Le but était d\'apprendre à mettre en place des bases de données, de créer une zone de recherche pour les visiteurs et de créer une partie pour les administrateurs, ainsi que l\'utilisation du framework Bootstrap.\n' + '\n',
    image: '/zelda.webp',
    url: 'https://zelda.leoturible.fr'
  },
  {
    id: 3,
    title: 'Ghibli',
    description: 'Ce site a été conçu sur le thème de l\'univers des studios Ghibli. Il a été réalisé en HTML, CSS et PHP dans le cadre d\'un projet en cours. Le but était de créer un formulaire fonctionnel et sécurisé, ainsi qu\'une gallerie d\'image avec la possibilité d\'en ajouter.\n' + '\n',
    image: '/ghibli.webp',
    url: 'https://ghibli.leoturible.fr'
  },
  {
    id: 4,
    title: 'Parooling',
    description: 'Ce site a été conçu dans le cadre d\'un projet en cours. Il a été réalisé en HTML, CSS et PHP. Le but était de créer un site de covoiturage avec un système de connexion et d\'inscription fonctionnel, ainsi qu\'un système de recherche de trajet.\n' + '\n',
    image: '/parooling_desktop.png',
    url: 'https://parooling.leoturible.fr'
  },
  {
    id: 5,
    title: 'Agenda',
    description: 'Ce site a été conçu dans le cadre d\'un projet en cours. Il a été réalisé avec le framework backend Symfony. Le but était de créer un site dédié aux étudiants de l\'IUT de Troyes, avec un système de connexion et d\'inscription fonctionnel, ainsi qu\'un système de calendrier pour ajouter des évènements.\n' + '\n',
    image: '/sae301.png',
    url: 'https://sae301.leoturible.fr'
  }
]

onMounted(() => {
  const phoneInput = document.getElementById('phone');
  phoneInput.addEventListener('input', function (e) {
    let value = e.target.value.replace(/\D/g, '');
    if (value.length > 10) {
      value = value.slice(0, 10);
    }
    value = value.replace(/(\d{2})(?=\d)/g, '$1 ');
    e.target.value = value;
  });
});
</script>

<template>
  <main class="snap-y snap-mandatory h-screen overflow-x-hidden">

    <section id="about" class="fade-in h-screen w-full flex flex-col items-center justify-center snap-start">
      <h1 class="mb-4 text-3xl font-extrabold text-gray-900 dark:text-white md:text-5xl lg:text-6xl ">
        <span class="text-transparent bg-clip-text bg-gradient-to-r to-emerald-300 from-sky-400">Léo Turible</span>
      </h1>
      <h2 class="text-4xl font-bold dark:text-white text-center">
        Full-Stack Developer Student
      </h2>
    </section>

    <section id="presentation" class="fade-in h-screen w-full flex flex-col items-center justify-around snap-center">
      <div class="w-full text-center self-start">
        <h2 class="mb-4 text-3xl font-extrabold text-gray-900 dark:text-white md:text-5xl lg:text-6xl text-center">
          Présentation</h2>
      </div>
      <div class="flex flex-col sm:flex-row flex-wrap items-center justify-center w-full">
        <div class="flex items-center justify-center sm:flex-1">
          <img src="/fallout.webp" alt="Photo de profil" class="w-48 h-48 rounded-full object-cover mb-4 sm:mb-0">
        </div>
        <div class="flex items-center justify-center sm:flex-1">
          <p class="text-gray-900 dark:text-white text-justify w-2/3">
            Bonjour, je suis Léo Turible, un étudiant en développement Full-Stack. J'ai une passion pour la création de
            solutions logicielles efficaces et l'apprentissage de nouvelles technologies.
          </p>
        </div>
      </div>
    </section>

    <section id="realisation" class="fade-in h-screen w-full flex flex-col items-center justify-around snap-center">
      <h2 class="text-4xl font-bold dark:text-white">Réalisations</h2>
      <RealisationSlider :cards="cards"/>
    </section>

    <section id="competence" class="fade-in h-screen w-full flex flex-col items-center justify-center snap-center">
      <h2 class="text-4xl font-bold dark:text-white">Compétences</h2>
      <SkillsComponent/>
    </section>

    <section id="contact" class="fade-in h-screen w-full flex flex-col items-center justify-around snap-center">
      <div class="w-full text-center self-start">
        <h2 class="mb-4 text-3xl font-extrabold text-gray-900 dark:text-white md:text-5xl lg:text-6xl text-center">
          Contact</h2>
      </div>
      <ContactForm/>
    </section>

  </main>
</template>

<style scoped>
main::-webkit-scrollbar {
  display: none;
}

main {
  scrollbar-width: none;
}
</style>

