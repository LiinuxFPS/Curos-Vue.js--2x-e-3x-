<template>
    <div>
        <h3>Componente Conteudo</h3>
        {{titulo}}
            <button @click="atualizar()">atualizar</button>
        <!-- Pascal case -->
        <Home></Home>
        <!-- camel case-->
        <publicar-vaga></publicar-vaga>
    </div>
</template>

<script>
    import Home from '../views/Home.vue'
    import PublicarVaga from '../views/PublicarVaga.vue';
    export default{
    name: 'Conteudo',
    data:()=>({
        titulo: '*'
    }),
    components: {
        Home,
        PublicarVaga
    },
    methods:{
        atualizar(){
            this.titulo += '*'
        }
    }
 }
</script>

<style>

</style>