<template>
    <ul class="profile-data">
        <li class="data-item">
            <Icon name="cloudTags" size="min(20pt, 6vw)" />
            <span>15</span>
        </li>
        <li class="data-item">
            <Icon name="account" size="min(20pt, 6vw)" />
            <span>15</span>
        </li>
        <li class="data-item">
            <Icon name="accountGroup" size="min(20pt, 6vw)" />
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
        gap: min(2px, 0.5vw);;
        align-items: center;
        color: white;
        font-size: min(12pt, 5vw);
        margin: v-bind(margin);
    }

    .profile-data .data-item {
        display: flex;
        align-items: center;
        gap: min(5px, 1.5vw);
        padding: min(5px, 2vw) min(10px, 2vw);
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