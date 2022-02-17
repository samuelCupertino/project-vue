<template>
    <button class="btn-toggle" @click="toggleTheme">
        <Icon 
            v-show="this.theme === 'light'" 
            class="icon-sunny" 
            name="WhiteBalanceSunny" 
            color="var(--secondary)" 
            size="min(18pt, 10vw)"
        />
        <Icon 
            v-show="this.theme === 'dark'"
            class="icon-night"
            name="WeatherNight"
            color="var(--secondary)"
            size="min(18pt, 10vw)"
        />
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
                theme: localStorage.theme
            }
        },
        created() {
            if(this.theme === 'dark') {
                document.body.classList.add('dark')
                return
            }
            this.theme = 'light'
        },
        methods: {
            toggleTheme() {
                const theme = this.theme === 'light' ? 'dark' : 'light'
                localStorage.theme = this.theme = theme
                document.body.classList.toggle('dark')
            }
        }
    }
</script>

<style scoped>
    .btn-toggle {
        border: none;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        color: var(--tertiary);
        background-color: transparent;
        position: relative;
        margin: v-bind(margin);
    }
    .btn-toggle::before {
        content: '';
        width: 100%;
        height: 2px;
        display: block;
        background-color: var(--tertiary);
        position: absolute;
    }
    .icon-sunny, .icon-night {
        background-color: var(--bgSecondary);
        border-radius: 50%;
        padding: 2px;
        font-size: min(18pt, 10vw);
        cursor: pointer;
        z-index: 1;
    }
</style>