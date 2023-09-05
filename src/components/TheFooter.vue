<script>
import BrandCarousel from './BrandCarousel.vue';


export default {
    components: { BrandCarousel },
    data() {
        return {
            FooterObj: [
                {
                    title: 'Address Info',
                    items: [
                        {
                            icon: 'fa-solid fa-location-dot',
                            contact: "60 29th Street San Francisco, CA 94110 705-Union Trade Center, United States of America"
                        },
                        {
                            icon: 'fa-solid fa-phone',
                            contact: '(+00) 123-456-789'
                        },
                        {
                            icon: 'fa-solid fa-envelope',
                            email: 'demo@example.com'
                        }
                    ]
                },
                {
                    title: 'Information',
                    items: [
                        { info: 'Bookmark' },
                        { info: 'Features' },
                        { info: 'Sitemap' },
                        { info: 'Lists' },
                        { info: 'Contact Us' },

                    ]
                },
                {
                    title: 'Extras',
                    items: [
                        { info: 'Delivery' },
                        { info: 'Cart' },
                        { info: 'Terms conditions' },
                        { info: 'My Account' },
                        { info: 'About us' }

                    ]
                },
                {
                    title: 'Our Newsletter',
                    items: [
                        { info_form: 'There are many variations of passanges of form humour or randomised' },
                        {
                            info_icon: [
                                "fa-brands fa-facebook-f",
                                "fa-brands fa-twitter",
                                "fa-brands fa-google-plus-g",
                                "fa-brands fa-skype",
                                "fa-brands fa-instagram"
                            ]
                        }


                    ]
                }
            ]

        }
    }
}

</script>
    
    
<template>
    <BrandCarousel></BrandCarousel>

    <footer class="pt-5 mt-5">
        <div class="container">
            <div class="row py-5 text-light">
                <div class="col-3" v-for="title in FooterObj">
                    <h5 class="fw-bold pb-3">{{ title.title }}</h5>
                    <div class="d-flex position-relative" v-for="info in title.items">
                        <i 
                        v-if="info.icon" 
                        :class="` lh-base ${info.icon} pe-3 `"
                        style="color: #f9aa01; font-size: 15px;"></i>
                        <a href="#">{{ info.email }}</a>
                        <span class="pb-3">{{ info.contact }}</span>
                        <p> {{ info.info }}</p>
                        <span>{{ info.info_form }}</span>

                        <div class="my-5 d-flex position-absolute top-50" v-if="info.info_form">
                            <input type="email" class="form-control border-0 rounded-0" id="exampleFormControlInput1"
                            placeholder="">
                            <button type="button" class="btn btn-light rounded-0">
                                <img src="public/newsletter.png" alt="">
                            </button>
                        </div>
                        <div v-for="icon in info.info_icon">
                            <a href="#" class="position-relative bottom-0"><i 
                                :class="`${icon} social`"></i></a>
                        </div>

                    </div>


                </div>

            </div>
        </div>
        <div class="w-100 border-top mb-3" style="border-color: rgba(128, 128, 128, 0.541);"></div>
        <div class="d-flex justify-content-between container">
            <div>
                <p class="text-light">Copyright <span><i class="fa-regular fa-copyright"></i></span> 2023 Codezeel</p>
            </div>
            <div class="px-3 overflow-hidden payment-span">
                <img class="px-1 express" src="src/assets/img/payments.png" alt="express">
                <img class="px-1 discover" src="src/assets/img/payments.png" alt="discover">
                <img class="px-1 master" src="src/assets/img/payments.png" alt="master">
                <img class="px-1 paypal" src="src/assets/img/payments.png" alt="paypal">
                <img class="px-1 visa" src="src/assets/img/payments.png" alt="visa">

            </div>
        </div>

    </footer>
</template>


<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;

footer {
    font-family: $secondary-font;
    background-image: url('public/footer-bg.png');
    background-size: cover;
    background-repeat: no-repeat;

    .social{
        padding: 0 .5rem;
        margin-top: 5rem;
    }

    .col-3{
        font-family: $primary-font;
        font-size: .9rem;
    }

    a {
        color: white;
        text-decoration: none;

        &:hover {
            color: $color-secondary;
        }
    }

    p {
        margin-bottom: .8rem;
        &:hover {
            color: $color-secondary;
        }
    }

    .list-group {
        border: 0;


        .list-group-item {
            background-color: transparent;
            color: white;
            border: 0;

            &:hover {
                color: $color-secondary;
            }

        }
    }

    .btn-light {
        background-color: white;
        border: 0;
        height: 37px;
        overflow-y: hidden;

        img {
            transform: translateY(3px);

            &:hover {
                transform: translateY(-61px);
            }
        }

    }

    .payment-span {
        height: 30px;

        .express {
            transform: translateY(-236px);
        }

        .discover {
            transform: translateY(-196px);

        }

        .master {
            transform: translateY(-38px);
        }

        .paypal {
            transform: translateY(-115px);
        }


    }

}
</style>