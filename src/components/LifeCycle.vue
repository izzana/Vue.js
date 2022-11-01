<template>
  <h1>Meu nome é: {{ nome }}</h1>
</template>

<script>
export default{
  name: 'LifeCycle',
  data() {
    return {
      nome: 'Ainda não sei',
    }
  },
  created() {//adicionando evento
    setTimeout(() => {//o nome vai mudar depois de alguns segundos
      this.nome = 'Mateus'
    }, 1000);

    this.lifeCycle()
  },
  mounted() {
    setTimeout(() => {//o nome vai mudar depois de alguns segundos
      this.nome = 'Pedro'
    }, 3000);

    this.lifeCycle()
  },
  methods: {
    lifeCycle() {
      console.log("Executou")
    }
  }
}
</script>