<template>
    <div>
        <h2>esta ŕ a descricao de: {{ nome }}</h2>
        <p>estou trabalhando dno momento.</p>
        <p>utilizo as segintes tescnologias:</p>
        <div v-if="isWorking">
            <ul>
                <li v-for="tech in technologies" :key="tech">{{ tech }}</li>
            </ul>
        </div>
        <a v-bind:href="profileLink">link</a>
    </div>
</template>

<script>
export default{
    name: 'Pessoa',
    data() {
        return {
            nome: 'samuel',
            isWorking: true,
            profileLink: 'https://github.com/samuelCupertino.png',
            technologies: ['JavaScript', 'Vue', 'Vuex', 'Vue Router', 'Vuex Router']
        }
    }
}
</script>
