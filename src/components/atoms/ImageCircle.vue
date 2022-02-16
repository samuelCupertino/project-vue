<template>
    <img :src="src" :alt="alt" class="image-circle" />
</template>

<script> 
    export default {
        name: 'ImageCircle',
        props: {
            src: {
                type: String,
                required: true
            },
            alt: {
                type: String,
                required: true
            },
            size: {
                type: String,
                default: '100%'
            },
            margin: {
                type: String,
                default: '0'
            },
            bgColor: {
                type: String,
                default: 'transparent'
            }
        }
    }
</script>

<style>
    .image-circle {
        aspect-ratio: 1;
        border-radius: 50%;
        object-fit: cover;

        width: v-bind(size);
        margin: v-bind(margin);
        background-color: v-bind(bgColor);
    }
</style>