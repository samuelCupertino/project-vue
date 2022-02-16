<template>
    <mdicon class="icon" :name="name" :size="size" :spin="spin"/>
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
                default: 24
            },
            spin: {
                type: Boolean,
                default: false
            }
        }
    }
</script>