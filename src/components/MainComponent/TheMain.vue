<script>
import FirstSection from "./FirstSectionComponent/FirstSection.vue";
import SecondSection from "./SecondSection.vue";
import ThirdSection from "./ThirdSectionComponent/ThirdSection.vue";
import FourthSection from "./FourthSectionComponent/FourthSection.vue";
import FifthSection from "./FifthSection.vue";
import SixthSection from "./SixthSection.vue";



export default {

    data() {
        return {

        }
    },

    components: {
    FirstSection,
    SecondSection,
    ThirdSection,
    FourthSection,
    FifthSection,
    SixthSection
},


}


</script>


<template>
    <FirstSection></FirstSection>
    <SecondSection></SecondSection>
    <ThirdSection></ThirdSection>
    <FourthSection></FourthSection>
    <FifthSection></FifthSection>
    <SixthSection></SixthSection>
    
    
</template>


<style lang="scss" scoped>
@use 'src/styles/partials/_mixins.scss' as *;


</style>