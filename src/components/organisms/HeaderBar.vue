<template>
    <header class="header">
        <SearchInput />
        <ToggleProfileVisibility />
    </header>
</template>
    
<script>
    import SearchInput from '../molecules/SearchInput.vue'
    import ToggleProfileVisibility from '../molecules/ToggleProfileVisibility.vue'
    
    export default {
        name: 'HeaderBar',
        components: {
            SearchInput,
            ToggleProfileVisibility
        }
    }
</script>

<style scoped>
    .header {
        grid-area: header;
        background-color: var(--bgSecondary);
        border-radius: 20px;

        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 20px;
        padding: 10px 20px;
    }
</style>
