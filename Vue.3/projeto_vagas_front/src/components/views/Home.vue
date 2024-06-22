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
                <indicador></indicador>
            </div>
            <div class="col-4">
                <div class="h-100 p-5 rounded-3 border bg-dark text-white">
                    <p>Profissionais cadastrados</p>
                    <h3>125</h3>
                </div>
            </div>
            <div class="col-4">
                <div class="h-100 p-5 rounded-3 border bg-info text-dark">
                    <p>Visitantes online</p>
                    <h3>12</h3>
                </div>
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