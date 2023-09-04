<script>
import BrandCarousel from './BrandCarousel.vue';


export default {
    components: { BrandCarousel }
}

</script>


<template>
    <BrandCarousel></BrandCarousel>

    <section class="pt-5 mt-5">
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
                        <a href="#" class="list-group-item list-group-item-action active" aria-current="true">
                            The current link item
                        </a>
                        <a href="#" class="list-group-item list-group-item-action">A second link item</a>
                        <a href="#" class="list-group-item list-group-item-action">A third link item</a>
                        <a href="#" class="list-group-item list-group-item-action">A fourth link item</a>
                        <a class="list-group-item list-group-item-action disabled" aria-disabled="true">A disabled link
                            item</a>
                    </div>
                </div>
                <div class="col-3">
                    <h5 class="fw-bold ps-3">Information</h5>
                    <div class="list-group">
                        <a href="#" class="list-group-item list-group-item-action active" aria-current="true">
                            The current link item
                        </a>
                        <a href="#" class="list-group-item list-group-item-action">A second link item</a>
                        <a href="#" class="list-group-item list-group-item-action">A third link item</a>
                        <a href="#" class="list-group-item list-group-item-action">A fourth link item</a>
                        <a class="list-group-item list-group-item-action disabled" aria-disabled="true">A disabled link
                            item</a>
                    </div>
                </div>
                <div class="col-3">
                    <h5 class="fw-bold ps-3">Information</h5>
                    <div class="list-group">
                        <a href="#" class="list-group-item list-group-item-action active" aria-current="true">
                            The current link item
                        </a>
                        <a href="#" class="list-group-item list-group-item-action">A second link item</a>
                        <a href="#" class="list-group-item list-group-item-action">A third link item</a>
                        <a href="#" class="list-group-item list-group-item-action">A fourth link item</a>
                        <a class="list-group-item list-group-item-action disabled" aria-disabled="true">A disabled link
                            item</a>
                    </div>
                </div>
            </div>

        </div>

    </section>
</template>


<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;

section {

    background-image: url('public/footer-bg.png');
    background-size: cover;
    background-repeat: no-repeat;

    .list-group {
        border: 0;

        .list-group-item {
            background-color: transparent;
            color: white;
            border: 0;
        }
    }


}
</style>