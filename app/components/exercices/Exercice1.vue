<template>
  <div class="text-white flex flex-col justify-center items-center p-2">
    <h1>{{ name }}</h1>
    <h1>{{ temp }}°</h1>
  </div>
</template>

<script setup>
const name = ref("");
const temp = ref("");
async function getWeather() {
  try {
    const response = await fetch(
      "https://prevision-meteo.ch/services/json/toulouse"
    );
    if (!response.ok) {
      throw new Error("Erreur");
    }
    const data = await response.json();
    console.log(data);
    return data;
  } catch (error) {
    console.error(error.message);
  }
}

onMounted(() =>
  getWeather().then((weather) => {
    if (weather) {
      name.value = weather.city_info.name;
      temp.value = weather.current_condition.tmp;
    }
  })
);
</script>
