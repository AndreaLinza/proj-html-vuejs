<script>

export default {

    data() {
        return {
            currentIndex: 0,
            itemsForPage: 5,

            img: [
                {
                    img_brand: "brand-01.png",
                },
                {
                    img_brand: "brand-02.png",
                },
                {
                    img_brand: "brand-03.png",
                },
                {
                    img_brand: "brand-04.png",
                },
                {
                    img_brand: "brand-05.png",
                },
                {
                    img_brand: "brand-01.png",
                }
            ],

        }

    },
    computed: {
        visibleBanner() {
            const startIndex = this.currentIndex;
            const endIndex = startIndex + this.itemsForPage;
            return this.img.slice(startIndex, endIndex);
        }
    },
    methods: {
        prevSlide() {


            if (this.currentIndex > 0) {
                this.currentIndex--;
            }
        },
        nextSlide() {
            const maxIndex = this.img.length - this.itemsForPage
            if (this.currentIndex < maxIndex) {
                this.currentIndex++;
            }
        }
    }

}
</script>


<template>
    <div class="slider container">
        <div class="row row-cols-lg-4 row-cols-md-2 g-4 mt-4" v-for="(brand, index) in visibleBanner" :key="index">
            <div class="category-card " :class="{ active: index === 0 }">
                <img :src="`${brand.img_brand} `" class="d-block" alt="">
            </div>
        </div>
        <button class="slider-control-prev" type="button" @click="prevSlide">
            <span class="slider-control-prev-icon ">
                <img src="arrow.png" alt="arrow">
            </span>
            <span class="visually-hidden">Previous</span>
        </button>
        <button class="slider-control-next" type="button" @click="nextSlide">
            <span class="slider-control-next-icon">
                <img src="arrow.png" alt="arrow">
            </span>
            <span class="visually-hidden">Next</span>
        </button>
    </div>
</template>


<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;

.slider {
    display: flex;
    justify-content: space-around;
    margin-bottom: 2rem;
    color: white;
    font-family: $secondary-font;
    position: relative;
    flex-wrap: nowrap;
    overflow-x: hidden;
    transition: .5s;

    img {
        padding: 0 2rem;
    }

    &:hover {
        .slider-control-prev {
            display: block;
        }

        .slider-control-next {
            display: block;
        }
    }

    .slider-control-prev {
        overflow: hidden;
        background-color: transparent;
        border: 0;
        height: 40px;
        width: 50px;
        position: absolute;
        top: 40%;
        left: 0px;


        img {

            padding: 0;
            transform: translateY(-45px);
            transition: .5s;

            &:hover {
                transform: translateY(8px);
                transition: .5s;
            }
        }
    }

    .slider-control-next {
        overflow: hidden;
        background-color: transparent;
        border: 0;
        height: 40px;
        width: 50px;
        position: absolute;
        top: 40%;
        right: -5px;


        img {
            transform: translate(-85px, -45px);

            transition: .5s;

            &:hover {
                transform: translate(-85px, 0);
                transition: .5s;
            }
        }

    }

    .category-card {

        position: relative;
    }



}
</style>