<template>
  <div
    class="text-white text-2xl flex flex-col justify-center items-center p-2"
  >
    <h1>{{ name }}</h1>
    <h1>{{ age }}</h1>
  </div>
</template>

<script setup>
defineProps({
  name: String,
  age: Number,
});
</script>
