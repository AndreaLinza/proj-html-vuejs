<script>

export default {

    data() {
        return {

            img:[
                {
                    img_brand:"brand-01.png",
                },
                {
                    img_brand:"brand-02.png",
                },
                {
                    img_brand:"brand-03.png",
                },
                {
                    img_brand:"brand-04.png",
                },
                {
                    img_brand:"brand-05.png",
                },
                {
                    img_brand:"brand-01.png",
                },
            ]

        }
    },

}
</script>


<template>
    <div id="carouselExampleAutoplaying" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-inner container"
        v-for="(brand, index) in img"
        :key="index">
            <div class="carousel-item"
            :class="{active : index === 0}">
                <img :src="`${brand.img_brand}`" class="d-block w-25" alt="">
            </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleAutoplaying"
            data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleAutoplaying"
            data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
        </button>
    </div>
</template>


<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;

.carousel-item {

    padding-top: 4rem;

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