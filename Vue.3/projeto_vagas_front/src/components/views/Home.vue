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
                <indicador titulo="Vagas abertas" indicador="100"></indicador>
            </div>
            <div class="col-4">
                <indicador titulo="Profissionais Cadastrados" indicador="225"></indicador>
            </div>
            <div class="col-4">
                <indicador titulo="Visitantes online" indicador="22"></indicador>
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
        }
    }
</script>


<style>

</style>