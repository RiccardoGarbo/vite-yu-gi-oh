<script>
import axios from 'axios'
import { store } from './data/store'
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons'
import AppPokémonList from './components/AppPokémonList.vue';
export default {
  components: { AppPokémonList },

  created() {
    axios.get(endpoint).then((res) => {
      store.pokemonList = res.data.docs
    })
  }

}

</script>

<template>
  <body class="vh-100 d-flex justify-content-center align-items-center bg-danger">
    <AppPokémonList />
  </body>
</template>
<style></style>
