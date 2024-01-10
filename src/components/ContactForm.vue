<script setup>
import { onMounted } from 'vue';

onMounted(() => {
  const phoneInput = document.getElementById('phone');
  phoneInput.addEventListener('input', function(e) {
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
  <div class="flex flex-col items-center justify-center w-full">
    <form class="flex flex-col items-center justify-center">
      <div class="grid gap-6 mb-6 md:grid-cols-2">
        <div>
          <label for="first_name"
                 class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Prénom</label>
          <input type="text" id="first_name"
                 class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                 placeholder="John" required>
        </div>
        <div>
          <label for="last_name" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Nom</label>
          <input type="text" id="last_name"
                 class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                 placeholder="Doe" required>
        </div>
      </div>
      <div class="w-full">
        <label for="phone" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Numéro de
          téléphone</label>
        <input type="tel" id="phone"
               class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
               placeholder="0X XX XX XX XX" pattern="(\d{2} ){4}\d{2}" required>
      </div>

      <div class="w-full">
        <label for="email" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Adresse
          email</label>
        <input type="email" id="email"
               class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
               placeholder="john.doe@company.com" required>
      </div>

      <div class="mb-6 w-full">
        <label for="message" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Votre
          message</label>
        <textarea id="message" rows="4"
                  class="block p-2.5 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                  placeholder="Écrivez vos pensées ici..."></textarea>
      </div>
      <button type="submit"
              class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm w-full sm:w-auto px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
        Envoyer
      </button>
    </form>
  </div>
</template>

<style scoped>

</style>