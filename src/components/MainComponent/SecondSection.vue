<script>

export default {


    data() {
        return {
            categorys: [
                {
                    img_category: 'category-image-01-446x550_t.jpg',
                    title_category: "PlayerUnknown's Battlegrounds"
                },
                {
                    img_category: 'category-image-02-446x550_t.jpg',
                    title_category: "Battefield"

                },
                {
                    img_category: 'category-image-03-446x550_t.jpg',
                    title_category: 'Jump Force'

                }
            ]
        }
    }


}

</script>


<template>
    <section>
        <div class="container">
            <h2 class="text-center text-light mt-5 fw-bold fs-1">Special Category</h2>
            <div class="d-flex justify-content-center"><span class="divider"></span></div>
            <div class="row row-cols-lg-3 row-cols-md-1 g-5">
                <div v-for="category in categorys">
                    <div class="category-card">
                        <img class="w-100" :src="`/${category.img_category}`" alt="">
                        <div class="hover-category">
                            <p>{{ category.title_category }}</p>
                            <a href="#">Shop Now</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>


<style lang="scss" scoped>
@use "src/styles/partials/_mixins.scss" as *;

section {

    font-family: $secondary-font;
    color: white;

    .divider{
        width: 100px;
        margin: 2rem 0;
        height: 2px;
        background-color: $color-secondary;
        
    }
    .category-card {

        position: relative;

        &:hover {
            .hover-category {

                background-color: rgb(23, 15, 32);
                transition: .5s;
            }

        }
    }

    .hover-category {
        position: absolute;
        margin: 0;
        padding: 1rem;
        bottom: 0;
        width: 100%;
        background-color: rgba(29, 20, 39, 0.418);
        transition: .5s;

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