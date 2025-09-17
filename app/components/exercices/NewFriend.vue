<template>
  <fieldset
    class="p-4 border rounded-lg max-w-md flex flex-col justify-center items-center w-full"
  >
    <label class="block"> Name </label>
    <input
      v-model="name"
      type="text"
      name="name"
      class="input border p-2 w-full mb-2"
      required
    />

    <label class="block"> Telephone </label>
    <input
      v-model="tel"
      type="text"
      name="tel"
      class="input border p-2 w-full mb-2"
      required
    />

    <label class="block"> Email </label>
    <input
      v-model="email"
      type="email"
      name="email"
      class="input border p-2 w-full mb-4"
      required
    />

    <button
      type="button"
      @click="send"
      class="bg-blue-600 text-white px-4 py-2 rounded-lg"
    >
      Ajouter un ami
    </button>
  </fieldset>
</template>

<script setup>
const emit = defineEmits(["newFriend"]);
const name = ref("");
const tel = ref("");
const email = ref("");

function send() {
  if (!name.value || !tel.value || !email.value) return;

  emit("newFriend", {
    id: Date.now().toString(),
    name: name.value,
    phone: tel.value,
    email: email.value,
    premium: false,
  });

  name.value = "";
  tel.value = "";
  email.value = "";
}
</script>
