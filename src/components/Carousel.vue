<script>

import TriangleTopBanner from './TriangleTopBanner.vue';

export default {

    components: {
        TriangleTopBanner
    }

}

</script>

<template>
    <div id="carouselExampleAutoplaying" class="carousel slide position-relative" data-bs-ride="carousel">

        <TriangleTopBanner></TriangleTopBanner>
        <div class="carousel-inner">
            <div class="carousel-item active">
                <img src="/red-dead-jumbo.jpg" class="d-block w-100" alt="Red-dead-redemption">
                <h2> Read Dead <br> Redemption 2</h2>
            </div>
            <div class="carousel-item">
                <img src="/hogwarts-legacy.jpg" class="d-block w-100" alt="Howarts-Legacy">
                <h2 class="my-position">Hogwarts <br>Legacy</h2>
            </div>
        </div>
        <button type="button" class="btn  shop-btn"><small>Shop Now</small></button>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleAutoplaying"
            data-bs-slide="prev">
            <span><i class="fa-solid fa-chevron-left"></i></span>
            <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleAutoplaying"
            data-bs-slide="next">
            <span><i class="fa-solid fa-chevron-right"></i></span>
            <span class="visually-hidden">Next</span>
        </button>


    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;



.carousel-item {

    position: relative;
    padding-top: 4rem;

    h2 {
        font-size: 4.5rem;
        position: absolute;
        text-align: center;
        top: 35%;
        right: 15%;
        font-family: $secondary-font;
        font-weight: 900;

    }

    .my-position {
        position: absolute;
        right: 22%;
    }

}

.shop-btn {
    position: absolute;
    padding: 0.4rem 1.5rem;
    z-index: 5;
    bottom: 26%;
    right: 30%;
    border-radius: 0;
    background-color: white;
    border-color: white;
    color: black;

    &:hover {
        @include default-button
    }

    &:active {
        @include default-button
    }



}

button {
    opacity: 1;

    span {
        font-size: 2.3rem;
        color: $color-secondary
    }
}
</style>