<script>
export default {
    name: 'Select-Type',
    props: { pokemonTypes: Array },
    emits: ['select-choice'],

}
</script>
<template>
    <select class="form-select " v-model="selectedType" @change="this.$emit('select-choice', this.selectedType)">
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