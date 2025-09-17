<template>
  <div class="min-h-screen bg-[#1a1b26] text-[#c0caf5] p-6 space-y-6">
    <!-- Header -->
    <h1
      class="text-center text-2xl text-[#7aa2f7] font-semibold animate-fade-in-down"
    >
      Exercice API onMounted et props
    </h1>

    <!-- Exercises grid -->
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
      <HelloWorld
        foo="toto"
        username="merci"
        class="bg-[#24283b] rounded-lg p-6 shadow-lg transition duration-300 hover:shadow-[0_0_15px_#7aa2f7] hover:border-[#7aa2f7] animate-fade-in-up"
      />

      <div
        class="bg-[#24283b] rounded-lg p-6 shadow-lg transition duration-300 hover:shadow-[0_0_15px_#9ece6a] hover:border-[#9ece6a] animate-fade-in-up delay-100"
      >
        <Exercice1 />
      </div>

      <div
        class="bg-[#24283b] rounded-lg p-6 shadow-lg transition duration-300 hover:shadow-[0_0_15px_#bb9af7] hover:border-[#bb9af7] animate-fade-in-up delay-200"
      >
        <Exercice2 />
      </div>
    </div>

    <!-- FriendsList full width card -->
    <div
      class="bg-[#1f2335] rounded-lg p-6 shadow-lg border border-[#565f89]/40 transition duration-300 hover:shadow-[0_0_20px_#7dcfff] hover:border-[#7dcfff] animate-fade-in-up delay-400"
    >
      <FriendsList />
    </div>

    <!-- TP full width card -->
    <div
      class="bg-[#1f2335] rounded-lg p-6 shadow-lg border border-[#565f89]/40 transition duration-300 hover:shadow-[0_0_15px_#e0af68] hover:border-[#e0af68] animate-fade-in-up delay-500"
    >
      <TP />
    </div>

    <div>
      <BarChart />
    </div>
  </div>
</template>

<script lang="ts" setup>
import Exercice1 from "~/components/exercices/Exercice1.vue";
import Exercice2 from "~/components/exercices/Exercice2.vue";
import FriendsList from "~/components/exercices/FriendsList.vue";
import HelloWorld from "~/components/exercices/HelloWorld.vue";
import TP from "~/components/exercices/TP-component.vue";
import BarChart from "~/components/exercices/BarChartDemo.vue";
</script>

<style>
@keyframes fade-in-up {
  0% {
    opacity: 0;
    transform: translateY(20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fade-in-down {
  0% {
    opacity: 0;
    transform: translateY(-20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fade-in-up {
  animation: fade-in-up 0.6s ease forwards;
}

.animate-fade-in-down {
  animation: fade-in-down 0.6s ease forwards;
}

/* Simple delay helpers */
.delay-100 {
  animation-delay: 0.1s;
}
.delay-200 {
  animation-delay: 0.2s;
}
.delay-300 {
  animation-delay: 0.3s;
}
.delay-400 {
  animation-delay: 0.4s;
}
.delay-500 {
  animation-delay: 0.5s;
}
</style>
