<template>
  <div
    class="bg-[#24283b] text-[#c0caf5] border border-[#565f89]/40 rounded-lg p-6 shadow-lg transition duration-300 hover:shadow-[0_0_20px_#7aa2f7] max-w-sm m-6"
  >
    <h2 class="text-lg font-semibold mb-3 text-[#7aa2f7]">
      {{ name }}
    </h2>

    <div class="space-y-2">
      <p class="text-[#9aa5ce]">
        {{ phone }}
      </p>

      <p class="font-bold text-[#c0caf5]">
        {{ email }}
      </p>

      <div v-if="premium" class="flex items-center mt-3">
        <span class="text-[#9ece6a] text-xl">✅</span>
        <span class="ml-2 text-sm text-[#9ece6a] font-medium">
          Premium Member
        </span>
      </div>

      <div class="flex gap-4 mt-4">
        <button
          class="font-bold rounded-lg text-lg uppercase w-32 h-16 bg-[#1f2335] text-[#c0caf5] hover:bg-[#24283b] hover:shadow-[0_0_10px_#f7768e] transition duration-300"
          @click.prevent="deleteFriend"
        >
          Supprimer
        </button>

        <button
          class="font-bold rounded-lg text-lg uppercase w-32 h-16 bg-[#1f2335] text-[#c0caf5] hover:bg-[#24283b] hover:shadow-[0_0_10px_#bb9af7] transition duration-300"
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
