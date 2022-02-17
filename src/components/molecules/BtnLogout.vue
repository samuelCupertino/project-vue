<template>
    <button class="btn-logout">
        <Icon class="search-icon" name="logout" size="32" />
    </button>
</template>

<script>
    import Icon from '../atoms/Icon.vue'

    export default {
        name: 'BtnLogout',
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
    .btn-logout {
        border:none;
        display: flex;
        align-items: center;
        justify-content: center;
        background-color: var(--bgTertiary);
        padding: 10px;
        border-radius: 20px;
        width: 90%;
        margin: 0 auto;
        aspect-ratio: 1;
        box-shadow: 2px 2px 2px var(--bgPrimary);
        cursor: pointer;
        transition: 0.5s;
    }
    .btn-logout:hover {
        box-shadow: 2px 2px 2px 2px var(--bgPrimary);
        transform: scale(1.1);
    }

    .search-icon {
        color: var(--textTertiary);
        transition-duration: 1.5s;
    }
    .btn-logout:hover .search-icon {
        color: var(--secondary);
    }
</style>