<template>
  <nav
    class="flex flex-col w-42 h-screen bg-black text-gray-800 border-r border-gray-200 shadow-sm"
  >
    <div class="px-6 py-6 border-b border-gray-100">
      <NuxtLink
        to="/"
        class="text-white text-lg font-medium hover:text-gray-600 transition-colors"
      >
        APP
      </NuxtLink>
    </div>

    <div class="flex-1 py-6">
      <div class="px-6">
        <h3
          class="text-xs font-semibold text-gray-400 uppercase tracking-wider mb-3"
        >
          Navigation
        </h3>
        <nav class="space-y-1">
          <NuxtLink
            to="/"
            class="flex items-center px-3 py-2 text-sm text-white hover:bg-gray-50 hover:text-gray-900 transition-colors"
          >
            Accueil
          </NuxtLink>
          <NuxtLink
            to="/Cours"
            class="flex items-center px-3 py-2 text-sm text-white hover:bg-gray-50 hover:text-gray-900 transition-colors"
          >
            Cours
          </NuxtLink>
          <NuxtLink
            to="/Exercices"
            class="flex items-center px-3 py-2 text-sm text-white hover:bg-gray-50 hover:text-gray-900 transition-colors"
          >
            Exercices
          </NuxtLink>
        </nav>
      </div>
    </div>

    <div class="px-6 py-4 border-t border-gray-100">
      <NuxtLink
        to="https://github.com/nuxt/ui"
        target="_blank"
        class="flex items-center px-3 py-2 text-sm text-gray-600 hover:bg-gray-50 hover:text-gray-900 transition-colors"
      >
        <Icon name="i-simple-icons-github" class="w-4 h-4 mr-2" />
        GitHub
      </NuxtLink>
    </div>
  </nav>
</template>
