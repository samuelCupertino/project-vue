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
            lineHeight: {
                type: String,
                default: 'normal'
            },
            maxLine: {
                type: Number,
                default: 999999
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
        line-height: v-bind(lineHeight);

        display: -webkit-box;
        overflow: hidden;
        text-overflow: ellipsis;
        -webkit-box-orient: vertical;
        -webkit-line-clamp: v-bind(maxLine);
    }
</style>