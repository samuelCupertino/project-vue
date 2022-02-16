<template>
    <div class="layout">
        <FavoriteBar />
        <Header />
        <ProfileBar />
        <Content />
    </div>
</template>
    
<script>
    import FavoriteBar from '../organisms/NavBar.vue'
    import Header from '../organisms/HeaderBar.vue'
    import ProfileBar from '../organisms/ProfileBar.vue'
    import Content from '../organisms/Content.vue'

    export default {
        name: 'Profile',
        components: {
            FavoriteBar,
            Header, 
            ProfileBar,
            Content
        }
    }
</script>

<style scoped>
    .layout {
        display: grid;
        grid-template-columns: 80px 1fr 250px;
        grid-template-rows: 60px auto;
        grid-template-areas:
            "favorite header profile"
            "favorite content profile";
        gap: 20px;

        width: 100vw;
        height: 100vh;
        overflow: hidden;

        padding: 20px;
        box-sizing: border-box;

        background-color: var(--bgPrimary);
    }
</style>