<script>
import Nav from './NavComponent/Nav.vue';
import JumboCarousel from './JumboCarousel.vue';


export default {

    components: {
        JumboCarousel,
        Nav,
    },

    

}


</script>

<template>
    <header>
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