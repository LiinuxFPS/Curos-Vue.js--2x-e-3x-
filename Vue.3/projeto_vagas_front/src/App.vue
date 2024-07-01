<template>
  <div>
    <topo v-on:TopoEnviaParaComponentePai="varRecebeEvent = $event"/>
    <conteudo v-if="visibilidade" :conteudo="varRecebeEvent" />
  </div>
</template>

<script>
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
    Topo
  }
}
</script>

<style>

</style>
