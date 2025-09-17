<template>
  <div>Exercice2</div>
  <h1>{{ pokemonName }}</h1>

  <h1>{{ pokemonWeight }}</h1>
</template>

<script setup>
const pokemonName = ref("");
const pokemonWeight = ref("");

async function getPokemon() {
  try {
    const response = await fetch("https://pokeapi.co/api/v2/pokemon/19/");
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

onMounted(() => {
  getPokemon().then((pokemon) => {
    if (pokemon) {
      pokemonName.value = pokemon.name;
      pokemonWeight.value = pokemon.weight;
    }
  });
});
</script>
