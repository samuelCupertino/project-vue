<template>
    <hr class="separator" />
</template>

<script> 
    export default {
        name: 'Separator',
        props: {
            margin: {
                type: String,
                default: '5px 0'
            },
            color: {
                type: String,
                default: 'var(--tertiary)'
            },
            height: {
                type: String,
                default: '2px'
            },
            width: {
                type: String,
                default: '100%'
            }
        }
    }
</script>

<style>
    .separator {
        border: none;
        border-radius: 50rem;
        width: v-bind(width);
        height: v-bind(height);
        margin: v-bind(margin);
        background: v-bind(color);
    }
</style>