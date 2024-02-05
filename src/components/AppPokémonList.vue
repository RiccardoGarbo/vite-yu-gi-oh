<script>
import PokémonCard from './PokémonCard.vue';
import { store } from '../data/store.js'
export default {
    name: 'PokémonList',
    components: { PokémonCard },
    data: () => ({
        store
    })
}

</script>
<template>
    <section id="pokémonList" class="container bg-secondary-subtle p-5">
        <div class="row h-100 d-flex flex-wrap bg-secondary">
            <div v-for="pokemon in store.pokemonList" class="col-2 h-50 d-flex align-items-center">
                <PokémonCard :pokemonName="pokemon.name" :pokemonNumber="pokemon.number" :image="pokemon.imageUrl"
                    :type="pokemon.type1" />
            </div>
        </div>

    </section>
</template>
<style>
#pokémonList {
    height: 75%
}

.col-2 {
    margin: 0 20px
}
</style>