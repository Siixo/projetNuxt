<template>
  <div
    class="bg-black text-white border border-gray-200/50 rounded-lg p-6 shadow-lg hover:shadow-xl transition-shadow duration-200 max-w-sm m-6"
  >
    <h2 class="text-lg font-semibold mb-3 text-white">
      {{ name }}
    </h2>

    <div class="space-y-2">
      <p class="text-gray-300">
        {{ phone }}
      </p>

      <p class="font-bold text-white">
        {{ email }}
      </p>

      <div v-if="premium" class="flex items-center mt-3">
        <span class="text-green-400 text-xl">✅</span>
        <span class="ml-2 text-sm text-green-400 font-medium">
          Premium Member
        </span>
      </div>
      <div class="flex gap-4 mt-4">
        <button
          class="font-bold rounded-lg text-lg uppercase w-32 h-16 bg-[#374151] text-[#ffffff] hover:cursor-pointer"
          @click.prevent="deleteFriend"
        >
          Supprimer
        </button>

        <button
          class="font-bold rounded-lg text-lg uppercase w-32 h-16 bg-[#374151] text-[#ffffff] hover:cursor-pointer"
          @click.prevent="changePremium"
        >
          Change
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps(["id", "name", "phone", "email", "premium"]);
const emit = defineEmits(["delete", "change"]);

function deleteFriend() {
  emit("delete", props.id);
}
function changePremium() {
  emit("change", props.id);
}
</script>
