<template>
    <main class="content">
        <CardUserRepo />
    </main>
</template>
    
<script>
    import CardUserRepo from '../molecules/CardUserRepo.vue'

    export default {
        name: 'Content',
        components: {
            CardUserRepo
        }
    }
</script>

<style scoped>
    .content {
        grid-area: content;
        display: flex;
        background-color: var(--bgSecondary);
        border-radius: 20px;

        height: calc(100vh - 160px);
        padding: 20px;
    }
</style>