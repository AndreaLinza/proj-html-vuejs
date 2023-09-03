<script>



export default {

    data() {
        return {


            currentPage: 0,
            itemsForPage: 4,
            list: [

                'Featured',
                'New Arrival',
                'Best Sellers'

            ],

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
                    price: '£83.00 - £90.00'
                },
                {
                    img_product: 'public/12-327x327.jpg',
                    discount: "",
                    vote: 2,
                    text_product: 'Labyrinths of th World',
                    first_price: '',
                    price: '£83.00 - £90.00'
                },
                {
                    img_product: 'public/12-327x327.jpg',
                    discount: "",
                    vote: 2,
                    text_product: 'Labyrinths of th World',
                    first_price: '',
                    price: '£83.00 - £90.00'
                },
                {
                    img_product: 'public/12-327x327.jpg',
                    discount: "",
                    vote: 2,
                    text_product: 'Labyrinths of th World',
                    first_price: '',
                    price: '£83.00 - £90.00'
                },
                {
                    img_product: 'public/12-327x327.jpg',
                    discount: "",
                    vote: 2,
                    text_product: 'Labyrinths of th World',
                    first_price: '',
                    price: '£83.00 - £90.00'
                },
                {
                    img_product: 'public/12-327x327.jpg',
                    discount: "",
                    vote: 2,
                    text_product: 'Labyrinths of th World',
                    first_price: '',
                    price: '£83.00 - £90.00'
                },
                {
                    img_product: 'public/12-327x327.jpg',
                    discount: "",
                    vote: 2,
                    text_product: 'Labyrinths of th World',
                    first_price: '',
                    price: '£83.00 - £90.00'
                },
                {
                    img_product: 'public/12-327x327.jpg',
                    discount: "",
                    vote: 2,
                    text_product: 'Labyrinths of th World',
                    first_price: '',
                    price: '£83.00 - £90.00'
                },
                {
                    img_product: 'public/12-327x327.jpg',
                    discount: "",
                    vote: 2,
                    text_product: 'Labyrinths of th World',
                    first_price: '',
                    price: '£83.00 - £90.00'
                },
            ]

        }
    },
    computed: {
        visibleProduct() {
            const startIndex = this.currentPage * this.itemsForPage;
            const endIndex = startIndex + this.itemsForPage;
            return this.listProduct.slice(startIndex, endIndex);
        }
    },
    methods: {
        prevSlide() {

            if (this.currentPage > 0) {
                this.currentPage--;
            }
            else if (this.currentPage = 0) {
                this.currentPage++
            }
        },
        nextSlide() {
            const maxPage = Math.ceil(this.listProduct.length / this.itemsForPage) - 1;
            if (this.currentPage < maxPage) {
                this.currentPage++;
            }
            else if (this.currentPage = maxPage) {
                this.currentPage = 0
            }
        },
    },



    // computed: {
    //     list() {
    //         return ['Featured', 'New Arrival', 'Best Sellers'];
    //     },
    // },







    };


</script>


<template>
    
        <!-- <section>
            <div class="container">
                <h2 class="text-center text-light mt-5 fw-bold fs-1">Our Product</h2>
                <div class="d-flex justify-content-center"><span class="divider"></span></div>
                <div class="list-group list-group-horizontal">
                    <a href="#" class="list-group-item" v-for="item in list">{{ item }}</a>
                </div>

                <carousel :per-page="4">
                    <slide v-for="(product, index) in listProduct" :key="index">
                        
                    </slide>
                </carousel>
            </div>
        </section> -->
    

    <section>
        <div class="container">
            <h2 class="text-center text-light mt-5 fw-bold fs-1">Our Product</h2>
            <div class="d-flex justify-content-center"><span class="divider"></span></div>
            <div class="list-group list-group-horizontal">
                <a href="#" class="list-group-item" v-for="item in list">{{ item }}</a>

            </div>
            <div class="slider-container">

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
                                <span>{{ product.vote }}</span>
                                <p class="fs-6">{{ product.text_product }}</p>
                                <span class="text-decoration-line-through pe-2" v-if="product.first_price">{{
                                    product.first_price }}</span>
                                <span style="color: #f9aa01;">{{ product.price }}</span>
                            </div>
                        </div>
                    </div>

                    <button class="slider-control-prev" type="button" @click="prevSlide">
                        <span class="slider-control-prev-icon "><i class="fa-solid fa-chevron-left"></i></span>
                        <span class="visually-hidden">Previous</span>
                    </button>
                    <button class="slider-control-next" type="button" @click="nextSlide">
                        <span class="slider-control-next-icon"><i class="fa-solid fa-chevron-right"></i></span>
                        <span class="visually-hidden">Next</span>
                    </button>
                </div>
            </div>
        </div>
    </section>
</template>


<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;

section {
    font-family: $secondary-font;

    .slider {
        position: relative;
        flex-wrap: nowrap;
        overflow-x: hidden;
        transition: .5s;


        .slider-control-prev {
            position: absolute;
            top: 50%;
        }

        .slider-control-next {
            position: absolute;
            top: 50%;
            right: 0;
        }
    }

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