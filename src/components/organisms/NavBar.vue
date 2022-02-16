<template>
    <aside class="favorite">
        <ImageCircle 
            src="https://project-base-react.vercel.app/_next/image?url=%2Fgithub-dark.png&w=256&q=75" 
            alt="Github logo" 
        />
        <Separator margin="10px 0"/>
        <FavoriteList margin="10px 0" />
        <BtnLogout />
    </aside>
</template>
    
<script>
    import ImageCircle from '../atoms/ImageCircle.vue'
    import Separator from '../atoms/Separator.vue'
    import FavoriteList from '../molecules/FavoriteList.vue'
    import BtnLogout from '../molecules/BtnLogout.vue'

    export default {
        name: 'NavBar',
        components: {
            ImageCircle,
            Separator,
            FavoriteList,
            BtnLogout
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