<script>

export default {

}
</script>


<template>
    <div id="carouselExampleAutoplaying" class="carousel slide" data-bs-ride="carousel">
        <div class="carousel-inner container ">
            <div class="carousel-item active">
                <img src="brand-01.png" class="d-block" alt="">
            </div>
            <div class="carousel-item">
                <img src="brand-02.png" class="d-block" alt="">
            </div>
            <div class="carousel-item">
                <img src="brand-03.png" class="d-block" alt="">
            </div>
            <div class="carousel-item ">
                <img src="brand-04.png" class="d-block" alt="">
            </div>
            <div class="carousel-item">
                <img src="brand-05.png" class="d-block" alt="">
            </div>
        </div>
        <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleAutoplaying"
            data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleAutoplaying"
            data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
        </button>
    </div>
</template>


<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;

.carousel-item {

padding-top: 4rem;

}

.shop-btn {
position: absolute;
padding: 0.4rem 1.5rem;
z-index: 5;
bottom: 26%;
right: 30%;
border-radius: 0;
background-color: white;
border-color: white;
color: black;

&:hover {
    @include default-button
}

&:active {
    @include default-button
}



}

button {
opacity: 1;

span {
    font-size: 2.3rem;
    color: $color-secondary
}
}
</style>