<script>
import axios from 'axios'
import AppPokémonList from './components/AppPokémonList.vue';
export default {
  components: { AppPokémonList }
}
</script>

<template>
  <body class="vh-100 d-flex justify-content-center align-items-center bg-danger">
    <AppPokémonList />
  </body>
</template>
<style></style>
