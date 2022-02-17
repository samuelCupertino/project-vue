<template>
    <h1 class="title">
        <slot />
    </h1>
</template>

<script> 
    export default {
        name: 'Title',
        props: {
            fontSize: {
                type: String,
                default: '16pt'
            },
            color: {
                type: String,
                default: 'var(--textPrimary)'
            },
            margin: {
                type: String,
                default: '0'
            },
        }
    }
</script>

<style>
    .title {
        font-size: v-bind(fontSize);
        color: v-bind(color);
        margin: v-bind(margin);
    }
</style>