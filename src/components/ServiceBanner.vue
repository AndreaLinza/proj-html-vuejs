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

        <div v-for="service in bannerService" 
        :class="`d-flex ${service.img}`">
            <div class="service-img">
                <img src="../assets/img/service-icon.png" alt="track">
            </div>
            <div class="d-flex flex-column text-start description">
                <strong>{{ service.title }}</strong>
                <span>{{ service.sub_title }}</span>
            </div>
        </div>

    </section>
</template>


<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

section {
    color: white;

    .description {
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