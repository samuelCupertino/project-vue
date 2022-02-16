<template>
    <button @click="toggleVisibility()">{{ btnText }}</button>
    <img v-show="isVisibly" :src="src" :alt="alt" />
</template>

<script>
export default {
    name: 'Picture',
    data() {
        return {
            src: '/favicon.ico',
            alt: 'favicon',
            isVisibly: true,
            btnText: 'esconder'
        }
    },
    methods: {
        toggleVisibility(ev) {
            this.isVisibly = !this.isVisibly
            this.btnText = this.isVisibly ? 'esconder' : 'mostrar'
        }
    }
}
</script>