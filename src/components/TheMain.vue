<script>
import FirstSection from "./FirstSection.vue";
import SecondSection from "./SecondSection.vue";
import ThirdSection from "./ThirdSection.vue";



export default {

    data() {
        return {

        }
    },

    components: {
    FirstSection,
    SecondSection,
    ThirdSection,

},


}


</script>


<template>
    <FirstSection></FirstSection>
    <SecondSection></SecondSection>
    <ThirdSection></ThirdSection>
    
    
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;


</style>