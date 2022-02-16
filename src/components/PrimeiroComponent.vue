<template>
  <h1>nome: {{nome}} sou um {{ profissao }}</h1>
</template>

<script>
  export default {
    name: 'PrimeiroComponent',
    data() {
      return {
        nome: 'samuel',
        profissao: 'programador'
      }
    }
  }
</script>
