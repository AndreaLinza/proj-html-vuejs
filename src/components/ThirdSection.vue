<script>
import ThirdSectionCarousel from './ThirdSectionCarousel.vue';



export default {


    components: {
        ThirdSectionCarousel
    },

    data() {
        return {



            list: [

                'Featured',
                'New Arrival',
                'Best Sellers'

            ],
            sliders:[
                {
                    img_slider:'cms-banner-03.jpg',
                    discount_banner: '20% Discount',
                    title_game:"Dragon's Dogma Video Game"

                },
                {
                    img_slider:'cms-banner-04.jpg',
                    discount_banner: 'Latest Game',
                    title_game:"World Of Tanks New Game"
                }
            ]


        }
    }
}


</script>


<template>
    <section>
        <div class="container-fluid">
            <h2 class="text-center text-light mt-5 fw-bold fs-1">Our Product</h2>
            <div class="d-flex justify-content-center"><span class="divider"></span></div>
            <div class="list-group list-group-horizontal">
                <a href="#" class="list-group-item" v-for="item in list">{{ item }}</a>

            </div>
            <ThirdSectionCarousel></ThirdSectionCarousel>
        </div>
        <div class="container my-5">
            <div class="banner-box">
                <div class="banner-img" v-for="slider in sliders">
                    <img :src="`${slider.img_slider}`" alt="">
                    <div class="banner d-flex">
                        <div class="triangle-left"></div>
                        <strong class="text-banner">{{ slider.discount_banner }}</strong>
                        <span class="triangle-right"></span>
                    </div>
                    <p class="text-img">{{ slider.title_game }}</p>
                </div>
            </div>
        </div>
    </section>
</template>


<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;

section {
    font-family: $secondary-font;

    .divider {
        width: 100px;
        margin: 2rem 0;
        height: 2px;
        background-color: $color-secondary;

    }

    .list-group {
        display: flex;
        justify-content: center;
        border-radius: 0;

        .list-group-item {
            background-color: transparent;
            color: white;
            transition: .5s;
            padding: 1rem 2.3rem;
            border-color: rgba(255, 255, 255, 0.151);

            &:hover {

                color: $color-secondary;
                transition: .5s;

            }

        }
    }

    .banner-box {
        display: flex;
        gap: 2rem;
        position: relative;
        font-family: 'Oxanium', cursive;

        .banner-img {
            width: calc(100% / 2 - 1rem);
            position: relative;
            overflow: hidden;

            .text-img {
                position: absolute;
                top: 35%;
                width: 45%;
                right: 5%;
                font-size: 2.3rem;
                font-weight: 900;
                color: white;

            }


            img {
                width: 100%;
                transition: 1s;

                &:hover {
                    transform: scale(1.10);
                }
            }
        }
    }

    .banner {
        position: absolute;
        z-index: 5;
        background-color: $color-secondary;
        top: 15%;
        right: 15%;

        .text-banner {
            font-style: italic;
            padding: 0 .3rem;
            font-size: 2rem;
            color: black;
        }

        .triangle-left {
            @include leftbanner-triangle-md;

        }

        .triangle-right {
            @include rightbanner-triangle-md;
        }
    }


}
</style>