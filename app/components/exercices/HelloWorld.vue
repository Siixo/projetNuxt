<script setup>
import { ref } from "vue";

// defineProps({
//   msg: String,
//   name: String,
// })

const props = defineProps(["foo", "username"]);

// console.log(props.foo)

const count = ref(0);
</script>

<template>
  <div class="text-white">
    <h1>Salut {{ foo }} - {{ username }}</h1>
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
