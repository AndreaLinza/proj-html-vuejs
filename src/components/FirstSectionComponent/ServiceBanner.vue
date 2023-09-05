<script>

export default {

    data() {
        return {
            bannerService: [

                {
                    img: 'track-img',
                    title: 'Free Delivery',
                    sub_title: 'Free Shipping On All Order',
                },
                {
                    img: 'moneybag-img',
                    title: 'Money Return',
                    sub_title: 'Back Guarantee in 7 days',
                },
                {
                    img: 'discount-img',
                    title: 'Member Discount',
                    sub_title: 'On every order over $130.00',
                },
                {
                    img: 'refound-img',
                    title: 'Return Policy',
                    sub_title: 'Support 24 hours a day'
                },

            ]
        }

    }

}
</script>


<template>
    <section class="container d-flex justify-content-around py-5">
        <div class="row row-cols-lg-4 row-cols-md-2 g-3">

            <div v-for="service in bannerService" :class="`${service.img}`">
                <div class="d-flex">
                    <div class="service-img">
                        <img src="src/assets/img/service-icon.png" alt="track">
                    </div>
                    <div class="description">
                        <strong class="w-100">{{ service.title }}</strong><br>
                        <span class="">{{ service.sub_title }}</span>
                    </div>
                </div>
            </div>
        </div>

    </section>
</template>


<style lang="scss" scoped>
@use "src/styles/partials/_mixins.scss" as *;

section {
    color: white;
    font-family: $primary-font;

    .description {
        width: 100%;

        &:hover {
            strong {
                color: $color-secondary ;
            }
        }
    }

    .track-img {
        .service-img {
            padding-right: 1rem;
            height: 50px;
            width: 100px;

            overflow-y: hidden;

            img {
                transform: translateY(-103px);
                transition: 1s;
            }
        }

        &:hover {
            img {
                transition: 1s;
                transform: translateY(10px);
            }
        }
    }

    .moneybag-img {
        .service-img {
            padding-right: 1rem;
            height: 50px;
            width: 100px;
            overflow-y: hidden;

            img {
                transform: translateY(-330px);
                transition: 1s;
            }
        }

        &:hover {
            img {
                transition: 1s;
                transform: translateY(-215px);
            }
        }
    }

    .discount-img {
        .service-img {
            padding-right: 1rem;
            height: 50px;
            width: 100px;
            overflow-y: hidden;

            img {
                transform: translateY(-555px);
                transition: 1s;
            }
        }

        &:hover {
            img {
                transition: 1s;
                transform: translateY(-440px);
            }
        }
    }

    .refound-img {
        .service-img {
            padding-right: 1rem;
            height: 50px;
            width: 100px;
            overflow-y: hidden;

            img {
                transform: translateY(-782px);
                transition: 1s;
            }
        }

        &:hover {
            img {
                transition: 1s;
                transform: translateY(-670px);
            }
        }
    }
}
</style>