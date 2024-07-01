<template>
  <div>
    <vagas-favoritas></vagas-favoritas>
    <topo v-on:TopoEnviaParaComponentePai="varRecebeEvent = $event"/>
    <conteudo v-if="visibilidade" :conteudo="varRecebeEvent" />
  </div>
</template>

<script>
import VagasFavoritas from './components/comuns/vagasFavoritas.vue';
import Conteudo from './components/layouts/Conteudo.vue'
import Topo from './components/layouts/Topo.vue';

export default {
  name: 'App',
  data:()=>({
    visibilidade: true,
    varRecebeEvent: 'Home'
  }),
  components: {
    Conteudo,
    Topo,
    VagasFavoritas
  }
}
</script>

<style>

</style>
