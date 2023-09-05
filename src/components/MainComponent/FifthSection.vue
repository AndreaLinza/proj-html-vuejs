<script>

export default {

    data() {
        return {
            personal: [
                {
                    icon: "t5-1-100x100_left.jpg",
                    name: "Luies Charls",
                    job: "(Web Desiner)",
                    description: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Corporis vero atque dolorem placeat.Repudiandae reiciendis laborum nulla veritatis, sequi suscipit incidunt quas quidem. Molestias, doloribus nisi. Impedit vero sint quam!"
                },
                {
                    icon: "t4-1-100x100_left.jpg",
                    name: "Din Desuza",
                    job: "(Iphone Developer)",
                    description: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Corporis vero atque dolorem placeat.Repudiandae reiciendis laborum nulla veritatis, sequi suscipit incidunt quas quidem. Molestias, doloribus nisi. Impedit vero sint quam!"
                },
                {
                    icon: "t2-1-100x100_left.jpg",
                    name: "Reema Ghurde",
                    job: "(Senior Manager)",
                    description: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Corporis vero atque dolorem placeat.Repudiandae reiciendis laborum nulla veritatis, sequi suscipit incidunt quas quidem. Molestias, doloribus nisi. Impedit vero sint quam!"
                }
            ]
        }
    }

}
</script>

<template>
    <section class="pb-4">

        <div id="carouselExampleIndicators" class="carousel slide">
            <div class="carousel-indicators">
                <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active"
                    aria-current="true" aria-label="Slide 1"></button>
                <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1"
                    aria-label="Slide 2"></button>
                <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2"
                    aria-label="Slide 3"></button>
            </div>
            <div class="carousel-inner container">
                <div class="carousel-item" 
                v-for="(person, index) in personal" 
                :key="index"
                :class="{ active : index === 0}">
                    <div class="quote"></div>
                    <img :src="`${person.icon}`" class="d-block profile-pic" alt="pic-1">
                    <div class="description-profile">
                        <p>{{ person.name }} <span style="color: #f9aa01;">{{ person.job }}</span></p>
                        <p>{{ person.description }}</p>
                    </div>
                </div>

            </div>
            <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators"
                data-bs-slide="prev">
                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Previous</span>
            </button>
            <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators"
                data-bs-slide="next">
                <span class="carousel-control-next-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Next</span>
            </button>
        </div>

    </section>
</template>

<style lang="scss" scoped>
@use "src/styles/partials/_mixins.scss" as *;


section {
    background-position: 10%;
    background-image: url('src/assets/img/parallax.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    color: white;

    .carousel-indicators {

        button {
            border-radius: 50%;
            width: 12px;
            height: 12px;
            margin: 0 .3rem;

        }

        .active {

            background-color: #f9aa01;
            border-radius: 50%;
            width: 12px;
            height: 12px;

        }
    }

    .carousel-inner {
        display: flex;
        padding: 2rem 0;

        .carousel-item {
            padding: 7rem 0;
            position: relative;

            .quote {
                position: absolute;
                padding: .8rem;
                background-image: url('quote.png');
                background-repeat: no-repeat;
                background-position: 6px;
                background-color: $color-secondary;
                border-radius: 50%;
                left: 50%;
                top: 24%;
                transform: translateX(-180%);
                z-index: 5;
            }

            .profile-pic {
                position: relative;
                left: 50%;
                transform: translateX(-50%);
                width: 100px !important;
                border-radius: 50%;
                border: 2px solid;
                border-color: $color-secondary;
            }

            .description-profile {
                text-align: center;
                padding: 0 10rem;

            }
        }

    }
}
</style>