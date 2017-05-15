<template>
  <P>
    Sobre a empresa... {{ msg }}. (Componente About)
  </P>
</template>

<script>
  export default {
    name: 'about',
    data () {
      return {
        msg: 'XPTO'
      }
    }
  }
</script>


<style scoped>
</style>
