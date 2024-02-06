<script>
export default {
    name: 'Select-Type',
    data: () => ({
        pokemonTypes: ["Bug", "Dark", "Dragon", "Electric", "Fairy", "Fighting", "Fire", "Flying", "Ghost", "Grass", "Ground", "Ice", "Normal", "Poison", "Psychic", "Rock", "Steel", "Water"],
        selectedType: ''
    })
}
</script>
<template>
    <select class="form-select " v-model="selectedType">
        <option selected>Scegli il tipo!</option>
        <option v-for="(type, i) in pokemonTypes" :key="i" :value="type">{{ type }}
        </option>
    </select>
</template>
<style scoped>
select {
    width: 200px;
}
</style>