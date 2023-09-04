<script>
import TheFooter from './components/TheFooter.vue';
import TheHeader from './components/TheHeader.vue';
import TheMain from './components/TheMain.vue';
export default {

  components: {
    TheHeader,
    TheMain,
    TheFooter
  }
}



</script>

<template>
  <TheHeader></TheHeader>
  <TheMain></TheMain>
  <TheFooter></TheFooter>
  <div class="rombo">
    <div class="btn-bg">
      <button type="button" class="btn return-btn"><a href="#"><i class="fa-solid fa-angles-up"
            style="color: black;"></i></a></button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../src/styles/partials/mixins" as *;

.rombo {
  position: fixed;
  bottom: 20px;
  right: 15px;
  width: 45px;
  height: 45px;
  -moz-transform: rotate(45deg) skew(10deg, 10deg);
  -webkit-transform: rotate(45deg) skew(10deg, 10deg);
  -ms-transform: rotate(45deg) skew(10deg, 10deg);
  -o-transform: rotate(45deg) skew(10deg, 10deg);
  transform: rotate(45deg) skew(10deg, 10deg);
  border: 2px solid $color-secondary;
}

.btn-bg {
  position: fixed;
  bottom: 3px;
  right: 3px;
  width: 35px;
  height: 35px;
  -moz-transform: rotate(45deg) skew(10deg, 10deg);
  -webkit-transform: rotate(45deg) skew(10deg, 10deg);
  -ms-transform: rotate(45deg) skew(10deg, 10deg);
  -o-transform: rotate(45deg) skew(10deg, 10deg);
  transform: rotate(0deg) skew(1deg, 1deg);
  background-color: $color-secondary;
}


button {
  border-radius: 0;


  &:active {
    border-color: transparent !important;

  }

  a {
    position: absolute;
    transform: rotate(315deg);
    font-size: 20px;
    top: 0px;
    right: 10px;

  }

}
</style>
