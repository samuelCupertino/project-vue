<template>
    <mdicon class="icon" :name="name" :spin="spin"/>
</template>

<script>
    export default {
        name: 'Icon',
        props: {
            name: {
                type: String,
                required: true
            },
            size: {
                type: Number,
                default: 'min(24pt, 6vw)'
            },
            spin: {
                type: Boolean,
                default: false
            }
        }
    }
</script>

<style>
    .icon.mdi {
        line-height: 0;
    }
    .icon.mdi > svg {
        width: v-bind(size);
        height: v-bind(size);
    }
</style>