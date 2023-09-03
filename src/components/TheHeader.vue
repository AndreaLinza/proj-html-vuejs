<script>
import TopBanner from './TopBanner.vue';
import Nav from './Nav.vue';
import Carousel from './Carousel.vue';


export default {

    components: {
        Carousel,
        TopBanner,
        Nav,
    },

    

}


</script>

<template>
    <header>
        <TopBanner></TopBanner>
        <Nav></Nav>
        <Carousel></Carousel>
    </header>
</template>

<style lang="scss" scoped>
@use "../src/styles/partials/variables" as *;

header {
    background-color: $color-primary;
    color: $color-text;
    font-family: $primary-font;
}
</style>