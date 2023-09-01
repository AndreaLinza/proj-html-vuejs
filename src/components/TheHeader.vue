<script>
import Nav from './Nav.vue';
import TopBanner from './TopBanner.vue';


export default {

    components: {
        TopBanner,
        Nav,
    },

    

}


</script>

<template>
    <header>
        <TopBanner></TopBanner>
    
        <Nav></Nav>
        

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