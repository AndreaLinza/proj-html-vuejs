<script>

export default {

    data() {
        return {
            currentIndex: 0,
            itemsForPage: 4,

            listProduct: [
                {
                    img_product: 'public/04-327x327.jpg',
                    discount: "-44%",
                    vote: 4,
                    text_product: 'Shopping Mahjong connect',
                    first_price: '£180.00',
                    price: '£100.00'

                },
                {
                    img_product: 'public/09-327x327.jpg',
                    discount: "",
                    vote: 0,
                    text_product: 'Buddy and Lucky Solitaire',
                    first_price: '',
                    price: '£83.00 - £90.00'
                },
                {
                    img_product: 'public/10-327x327.jpg',
                    discount: "",
                    vote: 0,
                    text_product: 'Taishou x Alice Epilogue',
                    first_price: '',
                    price: '£160.00'

                },
                {
                    img_product: 'public/11-327x327.jpg',
                    discount: "",
                    vote: 2,
                    text_product: 'Labyrinths of th World',
                    first_price: '',
                    price: '£110.00'
                },
                {
                    img_product: 'public/12-327x327.jpg',
                    discount: "-20%",
                    vote: 2,
                    text_product: "Reginald's Death Arena",
                    first_price: '£115.00',
                    price: '£92.00'
                },
                {
                    img_product: 'public/13-327x327.jpg',
                    discount: "-26%",
                    vote: 3,
                    text_product: 'Martin Goes on the Attack',
                    first_price: '£88.00',
                    price: '£65.00'
                },
                {
                    img_product: 'public/14-327x327.jpg',
                    discount: "",
                    vote: 0,
                    text_product: "What's in the Window",
                    first_price: '',
                    price: '£70.00'
                },
                {
                    img_product: 'public/15-327x327.jpg',
                    discount: "-10%",
                    vote: 0,
                    text_product: 'Legend of Mana Remastered',
                    first_price: '£100.00',
                    price: '£90.00'
                },
                {
                    img_product: 'public/16-327x327.jpg',
                    discount: "",
                    vote: 3,
                    text_product: 'Babol the Walking Box',
                    first_price: '',
                    price: '£75.00'
                },
                {
                    img_product: 'public/17-327x327.jpg',
                    discount: "-27%",
                    vote: 1,
                    text_product: 'Adam The Storyteller',
                    first_price: '£96.00',
                    price: '£70.00'
                },
                {
                    img_product: 'public/02-327x327.jpg',
                    discount: "-29%",
                    vote: 4,
                    text_product: 'The Little Tank Hunter',
                    first_price: '£85.00',
                    price: '£60.00'
                },
                {
                    img_product: 'public/03-327x327.jpg',
                    discount: "-20%",
                    vote: 2,
                    text_product: 'Train Station Renovation',
                    first_price: '',
                    price: '£92.00 - £110.00'
                },
            ]
        }

    },

    computed: {



        visibleProduct() {
            const startIndex = this.currentIndex;
            const endIndex = startIndex + this.itemsForPage;
            return this.listProduct.slice(startIndex, endIndex);
        }
    },
    methods: {
        starsVote(z) {

            const starsTot = 5


            const starVote = (z / starsTot) * 100

            return starVote
        },
        prevSlide() {
            const maxPage = this.listProduct.length - 4

            if (this.currentIndex > 0) {
                this.currentIndex--;
            }
            else {
                this.currentIndex = maxPage
            }
        },
        nextSlide() {
            const maxPage = this.listProduct.length - 4
            if (this.currentIndex < maxPage) {
                this.currentIndex++;
            }
            else {
                this.currentIndex = 0
            }
        }
    }

}

</script>

<template>
    <div class="slider container">
        <div class="slider row row-cols-4 g-4 mt-4">
            <div v-for="(product, i) in visibleProduct" :key="i">
                <div class="category-card">
                    <div class="discount d-flex">
                        <div class="triangle-left" v-if="product.discount"></div>
                        <strong class="text-banner">{{ product.discount }}</strong>
                        <span class="triangle-right" v-if="product.discount"></span>
                    </div>
                    <img class="w-100" :src="`${product.img_product}`" alt="">
                    <div class="hover-category">
                        <span class="stars-outer">
                            <div class="stars-inner" :style="`width:${starsVote(product.vote)}%;`"></div>

                        </span>
                        <p class="fs-6">{{ product.text_product }}</p>
                        <span class="text-decoration-line-through pe-2" v-if="product.first_price">{{
                            product.first_price }}</span>
                        <span style="color: #f9aa01;">{{ product.price }}</span>
                    </div>
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
    </div>
</template>


<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;

.slider {
    color: white;
    font-family: $secondary-font;
    position: relative;
    flex-wrap: nowrap;
    overflow-x: hidden;
    transition: .5s;

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
        left: -10px;
        display: none;

        img {
            transform: translateY(-50px);
            transition: .5s;

            &:hover {
                transform: translateX(0);
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
        display: none;

        img {
            transform: translate(-50px, -50px);

            transition: .5s;

            &:hover {
                transform: translate(-50px, 0);
                transition: .5s;
            }
        }

    }

    .category-card {

        position: relative;

        .discount {
            position: absolute;
            background-color: $color-secondary;
            top: 15px;
            left: 15px;


            .text-banner {
                font-style: italic;
                color: black;
            }

            .triangle-left {
                @include leftbanner-triangle-sm;

            }

            .triangle-right {
                @include rightbanner-triangle-sm;
            }
        }

    }

    .hover-category {

        margin: 0;
        padding: 1rem;
        bottom: 0;
        width: 100%;
        background-color: rgb(23, 15, 32);

        .stars-outer {
            display: inline-block;
            position: relative;
            font-family: FontAwesome;
        }

        .stars-outer::before {
            content: "\f006 \f006 \f006 \f006 \f006";
        }

        .stars-inner {
            position: absolute;
            top: 0;
            left: 0;
            white-space: nowrap;
            overflow: hidden;
            width: 0;
        }

        .stars-inner::before {
            content: "\f005 \f005 \f005 \f005 \f005";
            color: #f8ce0b;
        }


        p {
            font-size: 1.5rem;
        }

        a {
            color: $color-secondary;

            &:hover {
                text-decoration: none;
            }
        }

    }
}
</style>