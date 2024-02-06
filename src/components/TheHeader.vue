<script>
export default {
    name: 'The Header'
} </script>
<template>
    <div class="container d-flex justify-content-between py-3">
        <picture><img src="../../public/img/pokemon-logo.png" alt=""></picture>
        <select class="form-select ">
            <option selected>Scegli il tipo!</option>
            <option value="1">One</option>
            <option value="2">Two</option>
            <option value="3">Three</option>
        </select>
    </div>
</template>
<style scoped>
select {
    width: 200px;
}
</style>
