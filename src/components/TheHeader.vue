<script>
import AppSelectType from './AppSelectType.vue';
export default {
    name: 'The Header',
    components: { AppSelectType },
    emits: ['selected-choice'],
    data: () => ({
        pokemonTypes: ["Bug", "Dark", "Dragon", "Electric", "Fairy", "Fighting", "Fire", "Flying", "Ghost", "Grass", "Ground", "Ice", "Normal", "Poison", "Psychic", "Rock", "Steel", "Water"]

    })
} </script>
<template>
    <div class="container d-flex justify-content-between py-3">
        <picture><img src="../../public/img/pokemon-logo.png" alt=""></picture>
        <AppSelectType :pokemonTypes="pokemonTypes" @select-choice="$emit('selected-choice', $event)" />
    </div>
</template>
<style scoped></style>
