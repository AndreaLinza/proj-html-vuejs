<script>
import FirstSection from "./FirstSection.vue";
import SecondSection from "./SecondSection.vue";
import ThirdSection from "./ThirdSection.vue";
import FourthSection from "./FourthSection.vue";



export default {

    data() {
        return {

        }
    },

    components: {
    FirstSection,
    SecondSection,
    ThirdSection,
    FourthSection
},


}


</script>


<template>
    <FirstSection></FirstSection>
    <SecondSection></SecondSection>
    <ThirdSection></ThirdSection>
    <FourthSection></FourthSection>
    
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;


</style>