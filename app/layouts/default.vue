<template>
  <div>
    <AppNavbar />
    <main class="min-h-screen bg-black">
      <slot />
    </main>
    <AppFooter />
  </div>
</template>

<script lang="ts" setup>
import AppNavbar from "~/components/AppNavbar.vue";
import AppFooter from "~/components/AppFooter.vue";
</script>
