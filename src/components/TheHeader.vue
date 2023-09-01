<script>
import Nav from './Nav.vue';


export default {

    components: {
        Nav,
    },

    data() {
        return {
            navLink: [
                'Home',
                'Shop',
                'Blog',
                'Media',
                'ShortCode',
                'Feature',
            ],


        }
    }



}

</script>

<template>
    <header>
        <section class="py-3">
            <div class="container">
                <div class="d-flex justify-content-between">
                    <div class="d-flex">
                        <span class="mx-2">Wishlist (0)</span>
                        <span class="divider"></span>
                        <span class="mx-2 d-flex">Need Help?
                            <div class="nav-item dropdown">
                                <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
                                    aria-expanded="false">
                                    <i class="fa-solid fa-chevron-down"></i>
                                </a>
                                <ul class="dropdown-menu dropdown-menu-end dropdown-menu-lg-end">
                                    <li><a class="dropdown-item" href="#"></a></li>
                                    <li><a class="dropdown-item" href="#">0000-00-00</a></li>
                                    <li><a class="dropdown-item" href="#">9876543210</a></li>
                                    <li><a class="dropdown-item" href="#">9876-543-210</a></li>
                                    <li><a class="dropdown-item" href="#">+9876543210</a></li>
                                </ul>
                            </div>
                        </span>
                    </div>

                    <div>
                        <span>Call 24/7 . 800-8754-987</span>
                    </div>
                </div>
            </div>
        </section>
        <Nav :navLink="navLink" ></Nav>
        
    </header>
</template>

<style lang="scss" scoped>
@use "../src/styles/partials/variables" as *;

header {
    background-color: $color-primary;
    color: $color-text;
    font-family: $primary-font;



    section {
        border-bottom: 1px solid rgba(255, 255, 255, 0.233);


        .divider {

            display: flex;
            border-left: 1px solid rgba(255, 255, 255, 0.212);
            height: 10px;
            position: relative;
            top: 8px
        }

        span {
            color: gray;

            &:hover {
                color: $color-secondary
            }

            i {
                font-size: 10px;
                padding: 0 .5rem;
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
}
</style>