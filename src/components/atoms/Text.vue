<template>
    <p class="text">
        <slot />
    </p>
</template>

<script> 
    export default {
        name: 'Text',
        props: {
            fontSize: {
                type: String,
                default: '12pt'
            },
            color: {
                type: String,
                default: 'var(--textPrimary)'
            },
        }
    }
</script>

<style>
    .text {
        font-size: v-bind(fontSize);
        color: v-bind(color);
    }
</style>