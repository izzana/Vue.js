<template>
  <img :src="avatar" :alt="descricao">
</template>

<script>
  export default {
    name: 'Picture',
    data() {
      return {
        avatar: "/img/avatar.png", //sempre que eu colocar uma / ele vai estar linkando a minha pasta public
        descricao: "Nome da pessoa"
      }
    }
  }
</script>
