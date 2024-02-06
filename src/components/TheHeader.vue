<script>
import AppSelectType from './AppSelectType.vue';
export default {
    name: 'The Header',
    components: { AppSelectType },
    emits: ['selected-choice']
} </script>
<template>
    <div class="container d-flex justify-content-between py-3">
        <picture><img src="../../public/img/pokemon-logo.png" alt=""></picture>
        <AppSelectType @select-choice="$emit('selected-choice', $event)" />
    </div>
</template>
<style scoped></style>
