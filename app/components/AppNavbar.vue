<template>
  <nav
    class="flex justify-between items-center w-full bg-gray-900 text-white border-b-1 border-white p-4"
  >
    <div class="font-bold text-xl">
      <NuxtLink
        to="/"
        class="bg-white text-black p-4 rounded-2xl hover:bg-black hover:text-white"
        >APP</NuxtLink
      >
    </div>
    <div class="flex text-lg gap-4">
      <NuxtLink
        to="/"
        class="p-2 flex items-center hover:bg-white hover:text-black rounded-2xl"
      >
        Accueil
      </NuxtLink>
      <NuxtLink
        to="/Cours"
        class="p-2 flex items-center hover:bg-white hover:text-black rounded-2xl"
      >
        Cours
      </NuxtLink>
      <NuxtLink
        to="/Exercices"
        class="p-2 flex items-center hover:bg-white hover:text-black rounded-2xl"
      >
        Exercices
      </NuxtLink>
    </div>
    <div>
      <NuxtLink
        to="https://github.com/nuxt/ui"
        target="_blank"
        class="hover:bg-white hover:text-black transition-colors duration-200 p-2 rounded-2xl"
      >
        <Icon name="i-simple-icons-github" class="mr-2" />
        GitHub
      </NuxtLink>
    </div>
  </nav>
</template>
