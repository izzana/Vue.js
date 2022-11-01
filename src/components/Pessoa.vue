<template>
  <div>
    <h2>Está é a descrição da pessoa: {{ nome }} </h2>
    <Info />
    <Form />
  </div>
  
</template>

<script>
  import Info from "./Info.vue";//importando um componente
  import Form from "./Form.vue";
  export default {
    name: 'Pessoa',
    components: {
      Info,
      Form
    },
    data() {
      return {
        nome: 'Marcia'
      }
    }
  }
</script>