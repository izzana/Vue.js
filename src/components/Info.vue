<template>
  <div>
    <p>Estou trabalhando no momento.</p>
    <p>Utilizo as seguintes tecnologias:</p>
    <Linguagens />
    <div>
      <button @click="showEmail">{{ textoBotao }}</button>
    </div>
    <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
    <p class="teste">Para acessar meu portifólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui </a></p>
     <Picture />
  </div>
</template>

<script >
import Linguagens from "./Linguagens.vue";
import Picture from "./form/Picture.vue";
  export default {
    components: { Linguagens, Picture },
    name: 'Info',
    data() {
      return {
        esta_trabalhando: false,
        mostrar_email: false,
        email: 'email@email.com',
        meu_link: 'https://google.com',
        textoBotao: 'Mostrar email'
      }
    },
    methods: {
      showEmail() {
        //estou acessando o dado que o componente está exportando do data()
        this.mostrar_email = !this.mostrar_email //se eu clicar ele fica true, se clicar se novo fica false
        if(!this.mostrar_email) {
          this.textoBotao = 'Mostrar emai'
        } else {
          this.textoBotao = "Ocultar email"
        }
      }
    }
  }
</script>

<style>
  .paragrafo-pai {
    color: red;
  }
</style>