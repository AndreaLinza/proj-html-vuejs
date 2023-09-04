<script>



export default {

    data() {
        return {
            currentIndex: 0,
            itemsForPage: 3,

            listSlide: [
                {
                    img_slide: 'public/Nisi-ut-aliquid-ex-ea-com.jpg',
                    date:'Jan 18,2021',
                    comment: '0 Comment',
                    link: 'Shopping Mahjong connect'

                },
                {
                    img_slide: 'public/Architecto-beatae-vitae-dicta.jpg',
                    date:'Jan 18,2021',
                    comment: '0 Comment',
                    link: 'Shopping Mahjong connect'
                },
                {
                    img_slide: 'public/At-vero-eos-et-accusamus.jpg',
                    date:'Jan 18,2021',
                    comment: '0 Comment',
                    link: 'Shopping Mahjong connect'

                },
                {
                    img_slide: 'public/Blandit-praesen-volupta.jpg',
                    date:'Jan 18,2021',
                    comment: '0 Comment',
                    link: 'Shopping Mahjong connect'
                },
                {
                    img_slide: 'public/Consequunt-magni-dolores.jpg',
                    date:'Jan 18,2021',
                    comment: '0 Comment',
                    link: 'Shopping Mahjong connect'
                },
                {
                    img_slide: 'public/Et-quasi-architecto-beate.jpg',
                    date:'Jan 18,2021',
                    comment: '0 Comment',
                    link: 'Shopping Mahjong connect'
                },
                {
                    img_slide: 'public/Illo-inventore-veritatis-quasi.jpg',
                    date:'Jan 18,2021',
                    comment: '0 Comment',
                    link: 'Shopping Mahjong connect'
                },
                {
                    img_slide: 'public/Laborum-et-dolor-fuga-Et.jpg',
                    date:'Jan 18,2021',
                    comment: '0 Comment',
                    link: 'Shopping Mahjong connect'
                },
                {
                    img_slide: 'public/Omnis-iste-natus-error-sit.jpg',
                    date:'Jan 18,2021',
                    comment: '0 Comment',
                    link: 'Shopping Mahjong connect'
                },
                {
                    img_slide: 'public/Rerum-facilis-est-et-exped.jpg',
                    date:'Jan 18,2021',
                    comment: '0 Comment',
                    link: 'Shopping Mahjong connect'
                },

            ]
        }
    },
    computed: {
        visibleSlide() {
            const startIndex = this.currentIndex;
            const endIndex = startIndex + this.itemsForPage;
            return this.listSlide.slice(startIndex, endIndex);
        }
    },
    methods: {
        prevSlide() {
            const maxPage = this.listSlide.length - 3

            if (this.currentIndex > 0) {
                this.currentIndex--;
            }
            else {
                this.currentIndex = maxPage
            }
        },
        nextSlide() {
            const maxPage = this.listSlide.length - 3
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
    <section>
        <div class="container-fluid pt-5">
            <h2 class="text-center text-light mt-5 fw-bold fs-1">New Game Blogs</h2>
            <div class="d-flex justify-content-center"><span class="divider"></span></div>
        </div>
        <div class="container ">
            <div class="slider row row-cols-3 g-4 mt-2">
                <div v-for="(slide, i) in visibleSlide" :key="i">
                    <div class="category-card">
                        <img class="w-100" :src="`${slide.img_slide}`" alt="">
                        <div class="hover-category">
                            <span class="pe-2"> <i class="fa-regular fa-calendar-days" style="color: #f9aa01;"></i> {{  slide.date }} </span>
                            <span class="px-2"> <i class="fa-regular fa-comment" style="color: #f9aa01;"></i> {{ slide.comment }} </span><br>
                            <a href="#">{{ slide.link }}</a>
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
    </section>
</template>


<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;

section {
    font-family: $secondary-font;

    .container{
        border-bottom: 1px solid white;
    }

    .divider {
        width: 100px;
        margin: 2rem 0;
        height: 2px;
        background-color: $color-secondary;

    }




    .slider {
        margin-bottom: 2rem;
        color: white;
        font-family: $secondary-font;
        position: relative;
        flex-wrap: nowrap;
        overflow-x: hidden;


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



        }

        .hover-category {

            margin: 0;
            padding: 1rem;
            bottom: 0;
            width: 100%;
            background-color: rgb(23, 15, 32);
            a{
                color: white;
                text-decoration: none
            }

            a{
                &:hover{
                    color: $color-secondary;
                    
                }
            }

        }
    }
}
</style>