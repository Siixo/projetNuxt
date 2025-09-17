<template>
  <form class="space-y-4" @submit.prevent="submitForm">
    <div>
      <label>Nom:</label>
      <input v-model="name" type="text" required class="border rounded px-2" />
    </div>
    <div>
      <label>Âge:</label>
      <input
        v-model.number="age"
        type="number"
        required
        class="border rounded px-2"
      />
    </div>
    <button type="submit" class="bg-blue-600 text-white px-4 py-2 rounded">
      Valider
    </button>
  </form>
</template>

<script setup>
const emit = defineEmits(["update-user"]);

const name = ref("");
const age = ref("");

function submitForm() {
  emit("update-user", { name: name.value, age: age.value });
}
</script>
