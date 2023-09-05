<script>

import DropDownRight from './DropDownRight.vue';
import NavSelection from './NavSelection.vue';


export default {

    components: {
        DropDownRight,
        NavSelection,
    },

    data() {
        return {


        }
    }



}

</script>

<template>
    <nav class="navbar navbar-expand-lg">
        <div class="container justify-content-md-between py-2 px-1">

            <!-- Logo and hamburger -->
            <div >
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
                    data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false"
                    aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <a class="navbar-brand" href="#">
                    <img src="src/assets/img/logo.png" alt="">
                </a>
            </div>

            <!-- Central-nav  -->
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav m-auto">

                    <NavSelection></NavSelection>

                </ul>

            </div>

            <!-- Right-Navbar -->

            <div class="d-flex">
                <DropDownRight></DropDownRight>
            </div>
        </div>
    </nav>
</template>

<style lang="scss" scoped>
@use "src/styles/partials/_mixins.scss" as *;


.navbar {
    background-color: $color-primary;
    position: fixed;
    top:45px;
    width: 100%;
    z-index: 100;
    box-shadow: 10px 2px #8888886e;

    .container {

        justify-content: start;

        span {
            color: white
        }
    }

}
</style>