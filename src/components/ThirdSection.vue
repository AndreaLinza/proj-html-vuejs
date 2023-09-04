<script>
import FirstSectionCarousel from './FirstSectionCarousel.vue';



export default {


    components:{
        FirstSectionCarousel
    },

    data() {
        return {



            list: [

                'Featured',
                'New Arrival',
                'Best Sellers'

            ]


        }
    }
}


</script>


<template>
    <section>
        <div class="container-fluid">
            <h2 class="text-center text-light mt-5 fw-bold fs-1">Our Product</h2>
            <div class="d-flex justify-content-center"><span class="divider"></span></div>
            <div class="list-group list-group-horizontal">
                <a href="#" class="list-group-item" v-for="item in list">{{ item }}</a>

            </div>
            <FirstSectionCarousel></FirstSectionCarousel>
            
        </div>
    </section>
</template>


<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;

section {
    font-family: $secondary-font;

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

    
}
</style>