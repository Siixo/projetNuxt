<template>
  <div class="bg-gray-800">
    <div>
      <UserActive :name="name" :age="age" />
    </div>
    <div>
      <UserData @update-user="updateUser" />
    </div>
  </div>
</template>

<script setup>
import UserData from "./UserData.vue";
import UserActive from "./UserActive.vue";

const name = ref("Patrick Balkany");
const age = ref(72);

function updateUser(newUser) {
  name.value = newUser.name;
  age.value = newUser.age;
}
</script>
