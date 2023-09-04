<script>

export default {

}
</script>

<template>
    <section>

        <div id="carouselExampleIndicators" class="carousel slide">
            <div class="carousel-indicators">
                <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active"
                    aria-current="true" aria-label="Slide 1"></button>
                <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1"
                    aria-label="Slide 2"></button>
                <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2"
                    aria-label="Slide 3"></button>
            </div>
            <div class="carousel-inner">
                <div class="carousel-item active">
                    <div class="quote"></div>
                    <img src="t5-1-100x100_left.jpg" class="d-block profile-pic" alt="pic-1">
                    <div class="description-profile">
                        <p>Luies Charls <span style="color: #f9aa01;">(Web Desiner)</span></p>
                        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Corporis vero atque dolorem placeat.
                            Repudiandae reiciendis laborum nulla veritatis, sequi suscipit incidunt quas quidem. Molestias,
                            doloribus nisi. Impedit vero sint quam!</p>
                    </div>
                </div>
                <div class="carousel-item">
                    <div class="quote"></div>
                    <img src="t4-1-100x100_left.jpg" class="d-block profile-pic" alt="pic-2">
                    <div class="description-profile">
                        <p>Din Desuza <span>(Iphone Developer)</span></p>
                        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Corporis vero atque dolorem placeat.
                            Repudiandae reiciendis laborum nulla veritatis, sequi suscipit incidunt quas quidem. Molestias,
                            doloribus nisi. Impedit vero sint quam!</p>
                    </div>
                </div>
                <div class="carousel-item">
                    <div class="quote"></div>
                    <img src="t2-1-100x100_left.jpg" class="d-block profile-pic" alt="pic-3">
                    <div class="description-profile">
                        <p>Reema Ghurde <span>(Senior Manager)</span></p>
                        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Corporis vero atque dolorem placeat.
                            Repudiandae reiciendis laborum nulla veritatis, sequi suscipit incidunt quas quidem. Molestias,
                            doloribus nisi. Impedit vero sint quam!</p>
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
@use "../styles/partials/mixins" as *;


section {
    background-image: url('../assets/img/parallax.jpg');
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
                padding: 0 20rem;

            }
        }

    }
}
</style>