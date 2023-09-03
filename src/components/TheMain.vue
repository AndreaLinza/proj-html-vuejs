<script>
import FirstSection from "./FirstSection.vue";
import SecondSection from "./SecondSection.vue";



export default {

    data() {
        return {

        }
    },

    components: {

        FirstSection,
        SecondSection

    },


}


</script>


<template>
    <FirstSection></FirstSection>
    <SecondSection></SecondSection>
    
    
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;


</style>