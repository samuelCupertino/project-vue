<template>
    <div class="container" @click="toggleVisibility">
        <Icon class="icon-profile" name="accountCircle" size="min(24pt, 8vw)" />
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
        },
        methods: {
            toggleVisibility() {
                const layout = document.querySelector('.layout')
                layout.classList.toggle('profile-visible')
            }
        }
    }
</script>

<style scoped>
    .icon-profile {
        display: none;
    }
    
    @media (max-width: 768px) {
        .icon-profile {
            display: block;
            color: var(--textTertiary);
            cursor: pointer;
            transition-duration: 0.5s;
        }
        .icon-profile:hover,
        .layout.profile-visible .icon-profile {
            color: var(--secondary);
        }
    }
</style>