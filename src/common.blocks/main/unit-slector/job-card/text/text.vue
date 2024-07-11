<template>
    <p class="text">
        {{ text }}
    </p>
</template>

<script>
export default {
    name: 'TextView',
    props: {
        text: {
            type: String,
            require: true  
        }
    }
}
</script>

<style lang="scss" scoped>
    @import "./text"
</style>