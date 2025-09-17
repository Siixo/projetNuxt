<template>
  <nav
    class="flex flex-col w-42 h-screen bg-[#1a1b26] text-[#c0caf5] border-r border-[#565f89]/40 shadow-lg"
  >
    <!-- Logo / Header -->
    <div class="px-6 py-6 border-b border-[#565f89]/40">
      <NuxtLink
        to="/"
        class="text-[#7aa2f7] text-lg font-medium hover:text-[#9ece6a] transition-colors duration-300"
      >
        APP
      </NuxtLink>
    </div>

    <!-- Navigation links -->
    <div class="flex-1 py-6">
      <div class="px-6">
        <h3
          class="text-xs font-semibold text-[#565f89] uppercase tracking-wider mb-3"
        >
          Navigation
        </h3>
        <nav class="space-y-1">
          <NuxtLink
            to="/"
            class="flex items-center px-3 py-2 text-sm rounded-lg transition duration-300 hover:bg-[#24283b] hover:shadow-[0_0_10px_#7aa2f7] hover:text-[#7aa2f7]"
          >
            Accueil
          </NuxtLink>
          <NuxtLink
            to="/Cours"
            class="flex items-center px-3 py-2 text-sm rounded-lg transition duration-300 hover:bg-[#24283b] hover:shadow-[0_0_10px_#9ece6a] hover:text-[#9ece6a]"
          >
            Cours
          </NuxtLink>
          <NuxtLink
            to="/Exercices"
            class="flex items-center px-3 py-2 text-sm rounded-lg transition duration-300 hover:bg-[#24283b] hover:shadow-[0_0_10px_#bb9af7] hover:text-[#bb9af7]"
          >
            Exercices
          </NuxtLink>
        </nav>
      </div>
    </div>

    <!-- Footer / external link -->
    <div class="px-6 py-4 border-t border-[#565f89]/40">
      <NuxtLink
        to="https://github.com/nuxt/ui"
        target="_blank"
        class="flex items-center px-3 py-2 text-sm rounded-lg transition duration-300 hover:bg-[#24283b] hover:shadow-[0_0_10px_#7dcfff] hover:text-[#7dcfff]"
      >
        <Icon name="i-simple-icons-github" class="w-4 h-4 mr-2" />
        GitHub
      </NuxtLink>
    </div>
  </nav>
</template>
