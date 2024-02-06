<script>
import AppSelectType from './AppSelectType.vue';
export default {
    name: 'The Header',
    components: { AppSelectType }
} </script>
<template>
    <div class="container d-flex justify-content-between py-3">
        <picture><img src="../../public/img/pokemon-logo.png" alt=""></picture>
        <AppSelectType />
    </div>
</template>
<style scoped></style>
