<template>
    <div class="container">
        <Icon class="icon-profile" name="accountCircle" size="32" />
    </div>
</template>

<script>
    import Icon from '../atoms/Icon.vue'

    export default {
        name: 'ToggleProfileVisibility',
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
    .icon-profile {
        color: var(--textTertiary);
        cursor: pointer;
        transition-duration: 0.5s;
    }
    .icon-profile:hover {
        color: var(--secondary);
    }
</style>