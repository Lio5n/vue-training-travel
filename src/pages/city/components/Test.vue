<template>
    <div>
        <div class="px">我是像素</div>
        <div class="em">我是父相对</div>
        <div class="rem">我是根相对</div>
    </div>
</template>

<script>
    export default {
        name: "CityTest"
    }
</script>

<style lang="stylus" scoped>
    .em
        font-size 1em
    .rem
        font-size 1rem
</style>
