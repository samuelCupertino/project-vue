<template>
    <ul class="profile-data">
        <li class="data-item">
            <Icon name="cloudTags" />
            <span>15</span>
        </li>
        <li class="data-item">
            <Icon name="account" />
            <span>15</span>
        </li>
        <li class="data-item">
            <Icon class="icon" name="accountGroup" />
            <span>15</span>
        </li>
    </ul>
</template>

<script>
    import Icon from '../atoms/Icon.vue'

    export default {
        name: 'UserProfileData',
        props: {
            margin: {
                type: String,
                default: '0'
            }
        },
        components: {
            Icon
        }
    }
</script>

<style scoped>
    .profile-data {
        display: flex;
        justify-content: space-around;
        align-items: center;
        color: white;
        margin: v-bind(margin);
    }

    .profile-data .data-item {
        display: flex;
        align-items: center;
        gap: 5px;
        padding: 5px 10px;
        border-radius: 10px;
        cursor: pointer;

        transition-duration: 0.5s;
    }
    .profile-data .data-item:hover {
        background: var(--bgPrimary);
    }

    .profile-data .data-item .icon {
        color: var(--primary);
        transition-duration: 0.5s;
    }
    .profile-data .data-item:hover .icon {
        color: var(--secondary);
    }
</style>