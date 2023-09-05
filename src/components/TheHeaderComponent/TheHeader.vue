<script>
import TopBanner from './TopBanner.vue';
import Nav from './NavComponent/Nav.vue';
import JumboCarousel from './JumboCarousel.vue';


export default {

    components: {
        JumboCarousel,
        TopBanner,
        Nav,
    },

    

}


</script>

<template>
    <header>
        <TopBanner></TopBanner>
        <Nav></Nav>
        <JumboCarousel></JumboCarousel>
    </header>
</template>

<style lang="scss" scoped>
@use "src/styles/partials/_mixins.scss" as *;

header {
    background-color: $color-primary;
    color: $color-text;
    font-family: $primary-font;
}
</style>