<script setup>
const skills = [
  {
    category: 'Frontend',
    skills: [
      {name: 'HTML', icon: 'html5'},
      {name: 'CSS', icon: 'css3'},
      {name: 'JavaScript', icon: 'javascript'},
      {name: 'Sass', icon: 'sass'},
      {name: 'Tailwind CSS', icon: 'tailwindcss'},
      {name: 'Vue.js', icon: 'vuejs'},
    ],
  },
  {
    category: 'Backend',
    skills: [
      {name: 'PHP', icon: 'php'},
      {name: 'SYMFONY', icon: 'symfony'},
      {name: 'MYSQL', icon: 'mysql'},
    ],
  },
  {
    category: 'CMS',
    skills: [
      {name: 'WordPress', icon: 'wordpress'},
    ],
  },
  {
    category: 'Outils',
    skills: [
      {name: 'Git', icon: 'git'},
      {name: 'GitHub', icon: 'github'},
      {name: 'Visual Studio Code', icon: 'vscode'},
      {name: 'Figma', icon: 'figma'},
    ],
  },
];
</script>

<template>
  <div>
    <div v-for="skillGroup in skills" :key="skillGroup.category">
      <h3 class="text-2xl font-bold dark:text-white">{{ skillGroup.category }}</h3>
      <div class="skills-list">
        <div v-for="skill in skillGroup.skills" :key="skill.name" class="skill-item">
          <img :src="`/path/to/icons/${skill.icon}.svg`" alt="" class="skill-icon">
          <p>{{ skill.name }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.skills-list {
  display: flex;
  gap: 1rem;
}

.skill-item {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.skill-icon {
  width: 50px;
  height: 50px;
}
</style>