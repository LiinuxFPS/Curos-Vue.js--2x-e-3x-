<template>
    <div class="container py4">
        <div class="row">
            <div class="col">
                <!-- Componente PesquisarVaga -->
                <pesquisar-vaga></pesquisar-vaga>
            </div>
        </div>
        <div class="row mt-5">
            <!-- Vagas em aberto -->
            <div class="col-4">
                <indicador 
                    titulo="Vagas abertas" 
                    indicador="100"
                    bg="bg-dark"
                    color="text-white"></indicador>
            </div>
            <!-- Profissionais Cadastrados -->
            <div class="col-4">
                <indicador 
                    titulo="Profissionais Cadastrados" 
                    indicador="225"
                    bg="bg-dark"
                    color="text-white"></indicador>
            </div>
            <!-- Visitantes online -->
            <div class="col-4">
                <indicador 
                    titulo="Visitantes online" 
                    :indicador="usuariosOnline"
                    bg="bg-info"
                    color="text-dark"></indicador>
            </div>
        </div>
    </div>
</template>

<script>
    import PesquisarVaga from '@/components/comuns/PesquisarVaga.vue'
    import Indicador from '@/components/comuns/Indicador.vue';
    export default{
        name: 'Home',
        components:{
            PesquisarVaga,
            Indicador
        },
        data:()=>({
            usuariosOnline: 0
        }),
        methods:{
            getUsuariosOnline(){
                this.usuariosOnline = Math.floor(Math.random() * 101)
            } 
        },
        created(){
            setInterval(this.getUsuariosOnline, 3000)
        }
    }
</script>


<style>

</style>