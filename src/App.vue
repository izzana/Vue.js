<template>
  <div>
    <Header />
    <PrimeiroComponente />
    <p class="paragrafo-pai">O dado de app é {{ testando }}</p> 
    <LifeCycle />
    <Pessoa />
  </div>
</template>

<script>
  import Header from './components/Header';
  import PrimeiroComponente from './components/PrimeiroComponent';
  import LifeCycle from './components/LifeCycle';
  import Pessoa from './components/Pessoa';


  export default{
    name: 'App',
    components: {//tenho que especificar que vou ter componentes
      Header,
      PrimeiroComponente,
      LifeCycle,
      Pessoa
    },
    data() {
      return {
        testando: "Teste"
      }
    }
  }
</script>

<style>
  body {
    background-color: #333;
    color: #fff
  }
  a {
    color: red;
  }
  .teste {
    background-color: black;
  }
</style>