<script>
import ThirdSectionCarousel from './ThirdSectionCarousel.vue';
import { reactive } from 'vue';


export default {



    components: {
        ThirdSectionCarousel,

    },
    data() {

        const state = reactive({

            targetDate: new Date('2025-11-09'),
            currentTime: new Date(),
            countdownFinished: false,


        })
        const timeLeft = state.targetDate - state.currentTime;
        if (timeLeft <= 0) {
            state.countdownFinished = true;
            return {
                countDown: [
                    { time: 0 },
                    { time: 0 },
                    { time: 0 },
                    { time: 0 },
                ]
            }
        }


        const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
        const hours = Math.floor((timeLeft / (1000 * 60 * 60)) % 24);
        const minutes = Math.floor((timeLeft / 1000 / 60) % 60);
        const seconds = Math.floor((timeLeft / 1000) % 60);

        return {
            countDown: [
                { time: days, name: 'days' },
                { time: hours, name: 'hours' },
                { time: minutes, name: 'mins' },
                { time: seconds, name: 'secs' }
            ]
        }
    }



}

</script>


<template>
    <section>
        <div class="container-fluid">
            <h2 class="text-center text-light mt-5 fw-bold fs-1">Deal Of The Day</h2>
            <div class="d-flex justify-content-center"><span class="divider"></span></div>
            <div class="list-group list-group-horizontal">
                <a href="#" class="list-group-item" v-for="el in countDown">{{ el.time }} {{ el.name }}</a>
            </div>
            <ThirdSectionCarousel></ThirdSectionCarousel>
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

        }
    }



}
</style>