<template>
    <aside class="profile">
        <ImageCircle 
            src="https://github.com/samuelCupertino.png" 
            alt="foto de samuel cupertino" 
            size="85%"
            margin="5px 0"
        />
        <UserProfileName/>
        <UserProfileData margin="10px 0"/>
        <UserProfileRepos />
    </aside>
</template>
    
<script>
    import ImageCircle from '../atoms/ImageCircle.vue'
    import UserProfileData from '../molecules/UserProfileData.vue'
    import UserProfileName from '../molecules/UserProfileName.vue'
    import UserProfileRepos from '../molecules/UserProfileRepos.vue'
    
    export default {
        name: 'ProfileBar',
        components: {
            ImageCircle,
            UserProfileData,
            UserProfileName,
            UserProfileRepos
        }
    }
</script>

<style scoped>
    .profile {
        grid-area: profile;
        background-color: var(--bgSecondary);
        border-radius: 20px;
        padding: 20px 15px;

        height: calc(100vh - 40px);
        box-sizing: border-box;
            
        display: flex;
        flex-direction: column;
        align-items: center;
    }
</style>