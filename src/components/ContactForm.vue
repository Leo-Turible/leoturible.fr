<script setup>
import { onMounted, ref } from 'vue';
import emailjs from '@emailjs/browser';

const form = ref(null);
const formStatus = ref('');
const firstName = ref('');
const lastName = ref('');
const phone = ref('');
const email = ref('');
const message = ref('');

const sendEmail = (e) => {
  e.preventDefault();

  const templateParams = {
    first_name: firstName.value,
    last_name: lastName.value,
    phone: phone.value,
    email: email.value,
    message: message.value,
  };

  emailjs.send('service_ivxx1as', 'template_zsop8cf', templateParams, '8gQ4MOAmfUgFAI5Q1')
      .then((result) => {
        console.log(result.text);
        console.log(form.value);
        formStatus.value = 'Email envoyé avec succès !';
        // Réinitialiser les champs du formulaire
        firstName.value = '';
        lastName.value = '';
        phone.value = '';
        email.value = '';
        message.value = '';
      }, (error) => {
        console.log(error.text);
        console.log(form.value);
        formStatus.value = 'Échec de l\'envoi de l\'email. Veuillez réessayer.';
      });
}

onMounted(() => {
  const phoneInput = document.getElementById('phone');
  const formatPhone = function(e) {
    setTimeout(() => {
      let value = e.target.value.replace(/\D/g, '');
      if (value.length > 10) {
        value = value.slice(0, 10);
      }
      value = value.replace(/(\d{2})(?=\d)/g, '$1 ');
      e.target.value = value;
    }, 100);
  };
  phoneInput.addEventListener('input', formatPhone);
  phoneInput.addEventListener('change', formatPhone);
});


</script>

<template>
  <div class="flex flex-col items-center justify-center w-full">
    <form ref="form" @submit.prevent="sendEmail"  class="flex flex-col items-center justify-center mx-10 px-10 py-5 bg-slate-100 rounded-xl shadow-xl">
      <div class="grid gap-6 mb-6 md:grid-cols-2">
        <div>
          <label for="first_name"
                 class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Prénom</label>
          <input v-model="firstName" type="text" id="first_name"
                 class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                 placeholder="John" required>
        </div>
        <div>
          <label for="last_name" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Nom</label>
          <input v-model="lastName" type="text" id="last_name"
                 class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                 placeholder="Doe" required>
        </div>
      </div>
      <div class="w-full">
        <label for="phone" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Numéro de
          téléphone</label>
        <input v-model="phone" type="tel" id="phone"
               class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
               placeholder="0X XX XX XX XX" pattern="(\d{2} ){4}\d{2}" required>
      </div>

      <div class="w-full">
        <label for="email" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Adresse
          email</label>
        <input v-model="email" type="email" id="email"
               class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
               placeholder="john.doe@company.com" required>
      </div>

      <div class="mb-6 w-full">
        <label for="message" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Votre
          message</label>
        <textarea v-model="message" id="message" rows="4"
                  class="block p-2.5 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                  placeholder="Écrivez vos pensées ici..."></textarea>
      </div>
      <p v-show="formStatus" class="bg-blue-200 px-3.5 py-2 text-center rounded-lg mb-6">{{ formStatus }}</p>
      <button type="submit"
              class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm w-full sm:w-auto px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
        Envoyer
      </button>
    </form>
  </div>
</template>

<style scoped>

</style>