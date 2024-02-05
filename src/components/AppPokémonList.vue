<script>
import PokémonCard from './PokémonCard.vue';
export default {
    name: 'PokémonList',
    components: { PokémonCard }
}

</script>
<template>
    <section id="pokémonList" class="container bg-secondary-subtle p-5">
        <div class="row h-100 d-flex flex-wrap bg-secondary">
            <PokémonCard />
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