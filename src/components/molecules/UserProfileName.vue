<template>
    <div class="profile-name">
        <Title class="name">Samuel Cupertino</Title>
        <div class="login">
            <Text>@samuelCupertino</Text>
            <Icon class="icon-copy" name="contentCopy" size="16" margin />
        </div>
    </div>
</template>

<script>
    import Icon from '../atoms/Icon.vue'
    import Title from '../atoms/Title.vue'
    import Text from '../atoms/Text.vue'

    export default {
        name: 'UserProfileName',
        props: {
            margin: {
                type: String,
                default: '0'
            }
        },
        components: {
            Icon,
            Title,
            Text
        }
    }
</script>

<style scoped>
    .profile-name {
        color: white;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 2px;
        margin: v-bind(margin);
    }

    .profile-name .login {
        font-size: 12pt;
        display: flex;
        gap: 5px;
    }

    .icon-copy {
        color: var(--primary);
        cursor: pointer;
        transition-duration: 1s;
    }
    .icon-copy:hover {
        color: var(--secondary);
    }
</style>
