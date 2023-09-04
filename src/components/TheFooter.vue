<script>
import BrandCarousel from './BrandCarousel.vue';


export default {
    components: { BrandCarousel }
}

</script>


<template>
    <BrandCarousel></BrandCarousel>

    <footer class="pt-5 mt-5">
        <div class="container">
            <div class="row pt-5 text-light">
                <div class="col-3">
                    <h5 class="fw-bold">Address info</h5>
                    <p><i class="fa-solid fa-location-dot" style="color: #f9aa01; width: 10px;"></i> Lorem ipsum dolor
                        sit, amet consectetur adipisicing elit. Odit dolore aut rem corrupti libero corporis sapiente
                        architecto saepe consequatur deserunt ad quidem quod, sit explicabo ipsum possimus? Vero, quas
                        in!</p>
                    <p><i class="fa-solid fa-phone" style="color: #f9aa01;"></i> 000000000</p>
                    <p><i class="fa-solid fa-envelope" style="color: #f9aa01;"></i> ancascjac@gmial</p>
                </div>
                <div class="col-3">
                    <h5 class="fw-bold ps-3">Information</h5>
                    <div class="list-group">
                        <a href="#" class="list-group-item list-group-item-action" aria-current="true">
                            Bookmark
                        </a>
                        <a href="#" class="list-group-item list-group-item-action">Features</a>
                        <a href="#" class="list-group-item list-group-item-action">Sitemap</a>
                        <a href="#" class="list-group-item list-group-item-action">Lists</a>
                        <a href="#" class="list-group-item list-group-item-action">Contact Us</a>
                    </div>
                </div>
                <div class="col-3">
                    <h5 class="fw-bold ps-3">Extras</h5>
                    <div class="list-group">
                        <a href="#" class="list-group-item list-group-item-action" aria-current="true">
                            Delivery
                        </a>
                        <a href="#" class="list-group-item list-group-item-action">Cart</a>
                        <a href="#" class="list-group-item list-group-item-action">Terms conditions</a>
                        <a href="#" class="list-group-item list-group-item-action">My Account</a>
                        <a href="#" class="list-group-item list-group-item-action">About us</a>
                    </div>
                </div>
                <div class="col-3">
                    <h5 class="fw-bold">Our Newsletter</h5>

                    <span>There are many variations of passanges of form humour or randomised</span>

                    <div class="my-5 d-flex">
                        <input type="email" class="form-control border-0 rounded-0" id="exampleFormControlInput1"
                            placeholder="">
                        <button type="button" class="btn btn-light rounded-0">
                            <img src="public/newsletter.png" alt="">
                        </button>
                    </div>

                    <div class="list-group list-group-horizontal">
                        <a href="#" class="list-group-item list-group-item-action"><i
                                class="fa-brands fa-facebook-f"></i></a>
                        <a href="#" class="list-group-item list-group-item-action"><i class="fa-brands fa-twitter"></i></a>
                        <a href="#" class="list-group-item list-group-item-action"><i
                                class="fa-brands fa-google-plus-g"></i></a>
                        <a href="#" class="list-group-item list-group-item-action"><i class="fa-brands fa-skype"></i></a>
                        <a href="#" class="list-group-item list-group-item-action"><i
                                class="fa-brands fa-instagram"></i></a>
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

    background-image: url('public/footer-bg.png');
    background-size: cover;
    background-repeat: no-repeat;

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

    .payment-span{
        height: 30px;
        
        .express{
            transform: translateY(-236px);
        }
        .discover{
            transform: translateY(-196px);

        }
        .master{
            transform: translateY(-38px);
        }
        .paypal{
            transform: translateY(-115px);
        }

    
    }

}</style>