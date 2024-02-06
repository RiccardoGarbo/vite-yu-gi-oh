<script>
import axios from 'axios'
import { store } from './data/store'
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons'
import AppPokémonList from './components/AppPokémonList.vue';
import TheHeader from './components/TheHeader.vue';
import AppSelectType from './components/AppSelectType.vue';

export default {
  components: { AppPokémonList, TheHeader, AppSelectType },

  methods: {
    fetchPokemon(endpoint) {
      axios.get(endpoint).then((res) => {
        store.pokemonList = res.data.docs
      })
    },
    fetchPokemonType(type) {
      const typeEndPoint = `${endpoint}?eq[type1]=${type}`
      this.fetchPokemon(typeEndPoint)

    }
  },

  emits: ['selected-choice'],

  created() {
    this.fetchPokemon(endpoint)
  }

};

</script>

<template>
  <body class="vh-100 bg-danger">
    <TheHeader @selected-choice="fetchPokemonType" />
    <AppPokémonList />
  </body>
</template>
<style></style>
