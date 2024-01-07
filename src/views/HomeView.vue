<script setup>

</script>

<template>
  <main class="snap-y snap-mandatory h-screen overflow-x-hidden">
    <section id="about" class="h-screen w-full flex flex-col items-center justify-center snap-start">
      <h1 class="mb-4 text-3xl font-extrabold text-gray-900 dark:text-white md:text-5xl lg:text-6xl ">
        <span class="text-transparent bg-clip-text bg-gradient-to-r to-emerald-300 from-sky-400">Léo Turible</span>
      </h1>
      <h2 class="text-4xl font-bold dark:text-white">
        Full-Stack Developer Student
      </h2>
    </section>

    <section id="realisation" class="h-screen w-full flex flex-col items-center justify-center snap-center">
      <h2 class="text-4xl font-bold dark:text-white">Réalisations</h2>

      <div id="slider" class="flex flex-nowrap items-center justify-start gap-5 max-w-[80%] overflow-x-scroll snap-x snap-mandatory whitespace-nowrap">
          <div class="card-realisation snap-center flex flex-col items-center justify-center">
            <div class="card-realisation__img">
              <img src="https://picsum.photos/200/300" alt="">
            </div>
            <div class="card-realisation__content">
              <h3 class="card-realisation__title">Titre</h3>
              <p class="card-realisation__description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.</p>
            </div>
          </div>
          <div class="card-realisation snap-center flex flex-col items-center justify-center">
            <div class="card-realisation__img">
              <img src="https://picsum.photos/200/300" alt="">
            </div>
            <div class="card-realisation__content">
              <h3 class="card-realisation__title">Titre</h3>
              <p class="card-realisation__description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.</p>
            </div>
          </div>
          <div class="card-realisation snap-center flex flex-col items-center justify-center">
            <div class="card-realisation__img">
              <img src="https://picsum.photos/200/300" alt="">
            </div>
            <div class="card-realisation__content">
              <h3 class="card-realisation__title">Titre</h3>
              <p class="card-realisation__description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.</p>
            </div>
          </div>
          <div class="card-realisation snap-center flex flex-col items-center justify-center">
            <div class="card-realisation__img">
              <img src="https://picsum.photos/200/300" alt="">
            </div>
            <div class="card-realisation__content">
              <h3 class="card-realisation__title">Titre</h3>
              <p class="card-realisation__description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.</p>
            </div>
          </div>
          <div class="card-realisation snap-center flex flex-col items-center justify-center">
            <div class="card-realisation__img">
              <img src="https://picsum.photos/200/300" alt="">
            </div>
            <div class="card-realisation__content">
              <h3 class="card-realisation__title">Titre</h3>
              <p class="card-realisation__description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.</p>
            </div>
          </div>
          <div class="card-realisation snap-center flex flex-col items-center justify-center">
            <div class="card-realisation__img">
              <img src="https://picsum.photos/200/300" alt="">
            </div>
            <div class="card-realisation__content">
              <h3 class="card-realisation__title">Titre</h3>
              <p class="card-realisation__description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.</p>
            </div>
          </div>
          <div class="card-realisation snap-center flex flex-col items-center justify-center">
            <div class="card-realisation__img">
              <img src="https://picsum.photos/200/300" alt="">
            </div>
            <div class="card-realisation__content">
              <h3 class="card-realisation__title">Titre</h3>
              <p class="card-realisation__description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.</p>
            </div>
          </div>
          <div class="card-realisation snap-center flex flex-col items-center justify-center">
            <div class="card-realisation__img">
              <img src="https://picsum.photos/200/300" alt="">
            </div>
            <div class="card-realisation__content">
              <h3 class="card-realisation__title">Titre</h3>
              <p class="card-realisation__description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, voluptatum.</p>
            </div>
          </div>
      </div>
      
    </section>

    <section id="competence" class="h-screen w-full flex flex-col items-center justify-center snap-center">
      <h2 class="text-4xl font-bold dark:text-white">Compétences</h2>
      <p>
        Lorem ipsum dolor si
      </p>
    </section>

    <section id="contact" class="h-screen w-full flex flex-col items-center justify-around snap-center">
      <div class="w-full text-center self-start">
        <h2 class="mb-4 text-3xl font-extrabold text-gray-900 dark:text-white md:text-5xl lg:text-6xl text-center">
          Contact</h2>
      </div>
      <div class="flex flex-col items-center justify-center w-full">
        <form class="flex flex-col items-center justify-center">
          <div class="grid gap-6 mb-6 md:grid-cols-2">
            <div>
              <label for="first_name" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">First
                name</label>
              <input type="text" id="first_name"
                     class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                     placeholder="John" required>
            </div>
            <div>
              <label for="last_name" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Last
                name</label>
              <input type="text" id="last_name"
                     class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                     placeholder="Doe" required>
            </div>
          </div>
          <div class="w-full">
            <label for="phone" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Phone number</label>
            <input type="tel" id="phone"
                   class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                   placeholder="123-45-678" pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}" required>
          </div>

          <div class="w-full">
            <label for="email" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Email
              address</label>
            <input type="email" id="email"
                   class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                   placeholder="john.doe@company.com" required>
          </div>

          <div class="mb-6 w-full">
            <label for="message" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Your
              message</label>
            <textarea id="message" rows="4"
                      class="block p-2.5 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                      placeholder="Write your thoughts here..."></textarea>
          </div>
          <button type="submit"
                  class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm w-full sm:w-auto px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
            Submit
          </button>
        </form>
      </div>
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

