<script>

export default {

    data() {
        return {


        }
    }

}

</script>

<template>
    <div class="banner d-flex">
        <div class="triangle-left"></div>
        <strong class="text-banner">Upcoming Stock</strong>
        <span class="triangle-right"></span>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;

.banner {
    position: absolute;
    z-index: 10;
    background-color: $color-secondary;
    top: 25%;
    right: 25%;

    .text-banner {
        font-size: 2rem;
        color: black;
        padding: .3rem;
        font-family: 'Oxanium', cursive;
    }

    .triangle-left {
        @include leftbanner-triangle-lg;
    }

    .triangle-right {
        @include rightbanner-triangle-lg;
    }
}
</style>