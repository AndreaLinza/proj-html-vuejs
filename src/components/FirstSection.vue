<script>
import ServiceBanner from './ServiceBanner.vue';


export default {
    components: {
        ServiceBanner,

    },

    data() {
        return {
            sliders:[
                {
                    img_slider:'cms-banner-01.jpg',
                    title_banner: 'Most Popular',
                    title_game:'The Battlefield 4 Naval Strike'

                },
                {
                    img_slider:'cms-banner-02.jpg',
                    title_banner: 'Latest Game',
                    title_game:"Assassin's Creed Unity Game"
                }
            ]


        }
    }
}
</script>

<template>
    <ServiceBanner></ServiceBanner>

    <section class="container my-5">
        <div class="banner-box ">
            <div class="banner-img"
            v-for="slider in sliders">
                <img :src="`${slider.img_slider}`" alt="">
                <div class="banner d-flex">
                    <div class="triangle-left"></div>
                    <strong class="text-banner">{{slider.title_banner}}</strong>
                    <span class="triangle-right"></span>
                </div>
                <p class="text-img">{{slider.title_game}}</p>
            </div>
        </div>
    </section>
</template>


<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;

.banner-box {
    display: flex;
    gap: 2rem;
    position: relative;
    font-family: 'Oxanium', cursive;

    .banner-img {
        width: calc(100% / 2 - 1rem);
        position: relative;
        overflow: hidden;

        .text-img{
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
</style>

