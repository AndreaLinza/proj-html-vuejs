<script>
import Carousel from './Carousel.vue';
import { reactive, watch } from 'vue';


export default {



    components: {
        Carousel,

    },
    data() {

        const state = reactive({

            targetDate: new Date('2025-11-09'),
            currentTime: new Date(),
            countdownFinished: false,
            countDown: [
                { time: 0, name: 'days' },
                { time: 0, name: 'hours' },
                { time: 0, name: 'mins' },
                { time: 0, name: 'secs' },
            ]
        })

        const timingFunction = () => {

            const timeLeft = state.targetDate - state.currentTime;
            if (timeLeft <= 0) {
                state.countdownFinished = true;

                state.countDown = [
                    { time: 0, name: 'days' },
                    { time: 0, name: 'hours' },
                    { time: 0, name: 'mins' },
                    { time: 0, name: 'secs' },
                ]

                clearInterval(intervalId)

            }


            const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
            const hours = Math.floor((timeLeft / (1000 * 60 * 60)) % 24);
            const minutes = Math.floor((timeLeft / 1000 / 60) % 60);
            const seconds = Math.floor((timeLeft / 1000) % 60);

            state.countDown = [
                { time: days, name: 'days' },
                { time: hours, name: 'hours' },
                { time: minutes, name: 'mins' },
                { time: seconds, name: 'secs' }
            ]

        }

        const intervalId = setInterval(() => {
            state.currentTime = new Date();
            timingFunction()
        }, 1000);

        watch(() => state.targetDate, () => {
            timingFunction();
        });

        return {
            state
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
                <a href="#" class="list-group-item" v-for="el in state.countDown">{{ el.time }} {{ el.name }}</a>
            </div>
            <Carousel></Carousel>
        </div>
    </section>
</template>


<style lang="scss" scoped>
@use "src/styles/partials/_mixins.scss" as *;

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