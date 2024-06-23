<template>
    <!--div :class="`h-100 p-5 rounded-3 border ${bg} ${color}`"-->
    <div :class="estilo">
        <p>{{ titulo }}</p>
        <h3>{{ indicador }}</h3>
    </div>
</template>

<script>
export default {
    name: 'Indicador',
    props:['titulo', 'indicador','bg','color'],
    computed:{
        estilo(){
            //passsando o estilo como uma propriedade
            return `h-100 p-5 rounded-3 border ${this.bg} ${this.color}`
        }
    }
}
</script>

<style>

</style>