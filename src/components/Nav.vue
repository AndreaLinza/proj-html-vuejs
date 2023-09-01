<script>
import DropDown from './DropDown.vue';
import Search from './Search.vue';

export default {

    props: {
        navLink: {

            type: Array,
            required: true
        }
    },


    components: {
        DropDown,
        Search
    },

    data() {
        return {

            dropIcon: [
                'fa-magnifying-glass',
                'fa-dragon',
                'fa-bag-shopping'

            ],

            dropLink: {

                search: [

                ],
                account: [
                    'User Login',
                    'Checkout',
                ],
                cart:[
                    'No products in the cart.',
                ]
            }



        }
    }



}

</script>

<template>
    <nav class="navbar navbar-expand-lg">
        <div class="container py-2">

            <!-- Logo and hamburger -->
            <div>

                <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
                    data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false"
                    aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <a class="navbar-brand" href="#">
                    <img src="../assets/img/logo.png" alt="">
                </a>
            </div>

            <!-- Central-nav  -->
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav m-auto">
                    <li class="nav-item" v-for="link in navLink">
                        <a class="nav-link" aria-current="page" href="#">{{ link }}</a>
                    </li>
                </ul>

            </div>

            <!-- Right-Navbar -->

            <div class="d-flex">

                <DropDown></DropDown>
                <DropDown></DropDown>
                <DropDown></DropDown>

            </div>
        </div>
    </nav>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;


.navbar {
    background-color: $color-primary;

    .container {

        justify-content: start;

        span {
            color: white
        }

        li {
            padding: 0 2rem
        }

        a {
            color: $color-text;
        }


        .my-btn-outline {


            &:hover {
                a {
                    color: $color-secondary
                }
            }

        }

    }

}

.dropdown-menu {
    background-color: black;
    border-radius: 0;

    .dropdown-item {
        background-color: transparent;
        color: white;

        &:hover {
            color: $color-secondary
        }
    }

}

.dropdown-toggle {
    &:after {
        display: none;
    }
}
</style>