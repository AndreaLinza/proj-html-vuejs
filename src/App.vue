<script>
import ButtonUp from './ButtonUp.vue';
import TheFooter from './components/TheFooter.vue';
import TheHeader from './components/TheHeaderComponent/TheHeader.vue';
import TheMain from './components/MainComponent/TheMain.vue';
export default {

  components: {
    TheHeader,
    TheMain,
    TheFooter,
    ButtonUp
}
}



</script>

<template>
  <TheHeader></TheHeader>
  <TheMain></TheMain>
  <TheFooter></TheFooter>
  <ButtonUp></ButtonUp>
  
</template>

<style lang="scss" scoped>
@use "src/styles/partials/_mixins.scss" as *;


</style>
