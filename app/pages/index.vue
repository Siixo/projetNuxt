<template>
  <div class="p-8 bg-black h-full flex flex-col justify-center items-center">
    <h1 class="text-white text-4xl">Welcome to My Learning Platform</h1>
    <p class="text-white mt-4">Choose from our courses and exercises above!</p>
    <div class="flex mt-4 gap-4">
      <NuxtLink
        to="/Cours"
        class="group relative inline-block text-sm font-medium text-black focus:ring-3 focus:outline-hidden hover:cursor-pointer"
      >
        <span
          class="absolute inset-0 translate-x-0 translate-y-0 bg-gray-200 transition-transform group-hover:translate-x-0.5 group-hover:translate-y-0.5"
        />

        <span class="relative block border border-current bg-white px-8 py-3">
          Cours
        </span>
      </NuxtLink>
      <NuxtLink
        to="/Exercices"
        class="group relative inline-block text-sm font-medium text-black focus:ring-3 focus:outline-hidden hover:cursor-pointer"
      >
        <span
          class="absolute inset-0 translate-x-0 translate-y-0 bg-gray-200 transition-transform group-hover:translate-x-0.5 group-hover:translate-y-0.5"
        />

        <span class="relative block border border-current bg-white px-8 py-3">
          Exercices
        </span>
      </NuxtLink>
    </div>
  </div>
</template>
