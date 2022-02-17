<template>
    <aside class="favorite">
        <ImageCircle 
            src="https://project-base-react.vercel.app/_next/image?url=%2Fgithub-dark.png&w=256&q=75" 
            alt="Github logo" 
        />
        <BtnToggleTheme />
        <FavoriteList margin="10px 0" />
        <BtnLogout />
    </aside>
</template>
    
<script>
    import ImageCircle from '../atoms/ImageCircle.vue'
    import Icon from '../atoms/Icon.vue'
    import FavoriteList from '../molecules/FavoriteList.vue'
    import BtnLogout from '../molecules/BtnLogout.vue'
    import BtnToggleTheme from '../molecules/BtnToggleTheme.vue'

    export default {
        name: 'NavBar',
        components: {
            ImageCircle,
            FavoriteList,
            BtnLogout,
            Icon,
            BtnToggleTheme
        }
    }
</script>

<style scoped>
    .favorite {
        grid-area: favorite;
        background-color: var(--bgSecondary);
        border-radius: 30px;

        display: flex;
        flex-direction: column;
        padding: 15px 10px;
        height: calc(100vh - 40px);
        box-sizing: border-box;
    }

</style>