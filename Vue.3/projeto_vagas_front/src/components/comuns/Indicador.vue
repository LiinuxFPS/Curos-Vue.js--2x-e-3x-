<template>
    <div class="h-100 p-5 rounded-3 border bg-dark text-white">
        <p>{{ titulo }}</p>
        <h3>{{ indicador }}</h3>
    </div>
</template>

<script>
export default {
    name: 'Indicador',
    props:['titulo', 'indicador']
}
</script>

<style>

</style>