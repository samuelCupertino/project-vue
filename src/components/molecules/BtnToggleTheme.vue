<template>
    <button class="btn-toggle" @click="toggleTheme">
        <Icon v-if="isDark" class="icon-theme icon-night" name="WeatherNight" color="var(--secondary)"/>
        <Icon v-else class="icon-theme icon-sunny" name="WhiteBalanceSunny" color="var(--secondary)"/>
    </button>
</template>

<script>
    import Icon from '../atoms/Icon.vue'

    export default {
        name: 'BtnToggleTheme',
        props: {
            margin: {
                type: String,
                default: '0'
            }
        },
        components: {
            Icon
        },
        data() {
            return {
                isDark: false
            }
        },
        methods: {
            toggleTheme() {
                this.isDark = !this.isDark

                if (this.isDark) {
                    document.body.classList.add('dark')
                    return
                }

                document.body.classList.remove('dark')
            }
        }
    }
</script>

<style scoped>
    .btn-toggle {
        border: none;
        width: 100%;
        height: 2px;
        margin: 25px 0;
        display: flex;
        align-items: center;
        justify-content: center;
        color: var(--tertiary);
        background-color: var(--tertiary);
    }
    .icon-theme {
        background-color: var(--bgSecondary);
        border-radius: 50%;
        padding: 2px;
        cursor: pointer;
    }
</style>