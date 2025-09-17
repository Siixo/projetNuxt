<template>
  <footer
    class="flex justify-end items-center bg-[#1a1b26] text-[#c0caf5] p-4 border-t border-[#565f89]/40 rounded-t-lg shadow-inner"
  >
    <p
      class="transition duration-300 hover:text-[#7aa2f7] hover:drop-shadow-[0_0_8px_#7aa2f7]"
    >
      @Siixo 2025
    </p>
  </footer>
</template>

<script lang="ts" setup></script>

<style>
/* Optional: subtle fade-in on load */
@keyframes fade-in {
  0% {
    opacity: 0;
    transform: translateY(10px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

footer {
  animation: fade-in 0.6s ease forwards;
}
</style>
