<template>
  <nav
    class="flex justify-between items-center w-full px-4 py-2 bg-black text-white border-b-1 border-white"
  >
    <div class="flex gap-4">
      <ul class="flex gap-4">
        <li class="border-r-1 border-white p-2">
          <h1>Cours</h1>
        </li>
        <li>
          <h1>Exercices</h1>
        </li>
      </ul>
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
