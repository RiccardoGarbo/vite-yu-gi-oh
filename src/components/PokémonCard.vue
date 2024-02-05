<script>
export default {
    name: 'Pokémon Card',
    props: {
        pokemonName: String,
        image: String,
        type: String,
        pokemonNumber: Number


    }

}
</script>
<template>
    <div class="card p-4 text-center">
        <img class="rounded-circle " :src="image" :alt="pokemonName">
        <span>{{ pokemonNumber }}</span>
        <h5>{{ pokemonName }}</h5>
        <p class="fst-italic">{{ type }}</p>
    </div>
</template>
<style></style>