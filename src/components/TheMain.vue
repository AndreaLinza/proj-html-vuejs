<script>
import ServiceBanner from './ServiceBanner.vue';
import TriangleBanner from './TriangleBanner.vue';




export default {

    components: {
    ServiceBanner,
    TriangleBanner,

},


}


</script>


<template>
    <ServiceBanner></ServiceBanner>

    <section class="container my-5">
        <div class="banner-box">
            <div class="banner">
                <img src="../assets/img/cms-banner-01.jpg" alt="">
                <TriangleBanner></TriangleBanner>
            </div>
            <div class="banner">
                <img src="../assets/img/cms-banner-02.jpg" alt="">
            </div>
        </div>
    </section>

    <section>
        <div class="container">
            <h2 class="border-bottom text-center text-light my-5 py-5">Special Category</h2>
            <div class="row row-cols-3 g-5">
                <div>
                    <img src="../assets/img/category-image-01-446x550_t.jpg" alt="">
                </div>
                <div>
                    <img src="../assets/img/category-image-02-446x550_t.jpg" alt="">
                </div>
                <div>
                    <img src="../assets/img/category-image-03-446x550_t.jpg" alt="">
                </div>


            </div>
        </div>
    </section>
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.banner-box {
    display: flex;
    gap: 2rem;

    .banner {
        width: calc(100% / 2 - 1rem);

        overflow: hidden;


        img {
            width: 100%;
            transition: 1s;

            &:hover {
                transform: scale(1.10);
            }
        }
    }
}
</style>