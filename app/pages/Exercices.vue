<template>
  <div class="bg-black h-full text-white">
    <div
      class="grid grid-cols-5 grid-rows-[128px_300px_1fr] border border-gray-200/30 min-h-screen"
    >
      <h1
        class="col-span-5 text-center content-center text-2xl border-b border-gray-200/30 h-32"
      >
        Exercice API onMounted et props
      </h1>
      <HelloWorld
        foo="toto"
        username="merci"
        class="row-start-2 col-span-1 border border-gray-200/30 pl-4 flex flex-col justify-center items-center"
      />
      <div
        class="row-start-2 col-start-2 border border-gray-200/30 flex flex-col items-center justify-center p-4"
      >
        <Exercice1 />
      </div>
      <div
        class="row-start-2 col-start-3 border border-gray-200/30 flex flex-col items-center justify-center p-4"
      >
        <Exercice2 />
      </div>
      <div
        class="row-start-2 col-start-4 col-span-2 border border-gray-200/30 flex items-center justify-center p-4"
      >
        <div class="text-gray-400">Additional content here</div>
      </div>
      <!-- FriendsList now properly positioned in row 3 -->
      <div
        class="row-start-3 col-span-5 border border-gray-200/30 p-4 overflow-auto flex"
      >
        <FriendsList />
      </div>
      <div>
        <TP />
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import Exercice1 from "~/components/exercices/Exercice1.vue";
import Exercice2 from "~/components/exercices/Exercice2.vue";
import FriendsList from "~/components/exercices/FriendsList.vue";
import HelloWorld from "~/components/exercices/HelloWorld.vue";
import TP from "~/components/exercices/TP-component.vue";
</script>

<style></style>
