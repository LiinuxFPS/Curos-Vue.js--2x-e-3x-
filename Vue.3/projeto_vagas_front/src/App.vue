<template>
  <div>
    <vagas-favoritas></vagas-favoritas>
    <topo v-on:TopoEnviaParaComponentePai="varRecebeEvent = $event"/>
    <alerta v-if="exibirAlerta">
      <!-- passando conteudo HTML para o componente por meio de <slots></slot> -->
      <div class="alert alert-success" role="alert">
        <h4>Vaga publicada</h4>
        <p>Sua vaga foi Publicada com sucesso !</p>
      </div>
    </alerta>
    <conteudo v-if="visibilidade" :conteudo="varRecebeEvent" />
  </div>
</template>

<script>
import Alerta from './components/comuns/Alerta.vue';
import VagasFavoritas from './components/comuns/vagasFavoritas.vue';
import Conteudo from './components/layouts/Conteudo.vue'
import Topo from './components/layouts/Topo.vue';

export default {
  name: 'App',
  data:()=>({
    visibilidade: true,
    varRecebeEvent: 'Home',
    exibirAlerta: false
  }),
  components: {
    Conteudo,
    Topo,
    VagasFavoritas,
    Alerta
  },
  mounted(){
    this.emitter.on('alerta', ()=>{
      this.exibirAlerta = true
      setTimeout(()=>this.exibirAlerta = false, 3000)
    })
  }
}
</script>

<style>

</style>
