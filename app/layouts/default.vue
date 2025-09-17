<template>
  <div class="flex flex-col h-screen">
    <!-- Main horizontal layout -->
    <div class="flex flex-1">
      <!-- Sidebar (your navbar) -->
      <AppNavbar class="fixed left-0 top-0 h-screen z-50" />

      <!-- Main content area -->
      <main class="flex-1 overflow-y-auto ml-42">
        <slot />
      </main>
    </div>

    <!-- Footer spans full width at bottom -->
    <AppFooter />
  </div>
</template>

<script lang="ts" setup>
import AppNavbar from "~/components/AppNavbar.vue";
import AppFooter from "~/components/AppFooter.vue";
</script>
