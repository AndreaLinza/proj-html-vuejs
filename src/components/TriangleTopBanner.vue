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
        border-right: 0px solid #f9aa01;
        border-bottom: 56px solid #f9aa01;
        border-left: 18px solid transparent;
        border-top: 17px solid transparent;
        position: absolute;
        left: -18px;
        top: -15px;


    }

    .triangle-right {
        border-right: 0px solid #f9aa01;
        border-bottom: 56px solid #f9aa01;
        border-left: 18px solid transparent;
        border-top: 18px solid transparent;
        position: absolute;
        transform: rotate(180deg);
        right: -18px;
        top: 0;
    }
}
</style>