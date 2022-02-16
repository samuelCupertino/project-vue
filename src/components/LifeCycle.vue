<template>
    <h1>meu nome e: {{ nome }}</h1>
</template>

<script>
export default{
    name: 'PrimeiroComponent',
    data() {
        return {
            nome: 'ainda nao sei'
        }
    },
    created() {
        this.nome = 'samuel'
        console.log('Componente criado')
    },
}
</script>
