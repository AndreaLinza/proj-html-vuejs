<script>

export default {

    data() {

        return {

            contacts: [
                {
                    icon: "fa-phone",
                    number: "0000-00-00"

                },
                {
                    icon: "fa-phone",
                    number: "9876543210"

                },
                {
                    icon: "fa-brands fa-whatsapp",
                    number: "9876-543-210"

                },
                {
                    icon: "fa-brands fa-skype",
                    number: "+9876543210"

                },

            ]


        }
    }
}

</script>

<template>
    <section class="py-3">
        <div class="container">
            <div class="d-flex justify-content-between">
                <div class="d-flex align-items-center">
                    <span class="mx-2">Wishlist (0)</span>
                    <span class="divider"></span>
                    <span class="btn-group d-flex">
                        <button class="btn dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
                            Need Help?
                            <i class="fa-solid fa-chevron-down"></i>
                        </button>
                        <ul class="dropdown-menu">
                            <li v-for="contact in contacts">
                                <a class="dropdown-item" href="#">
                                    <i :class="`fa-solid ${contact.icon}`"></i>
                                    {{ contact.number }}</a>
                            </li>
                        </ul>
                    </span>
                    <!-- <span class="mx-2 d-flex">
                        <div class="nav-item dropdown">
                            <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
                                aria-expanded="false">
                                <i class="fa-solid fa-chevron-down"></i>
                            </a>
                            <ul class="dropdown-menu dropdown-menu-end dropdown-menu-lg-end">
                                <li v-for="contact in contacts">
                                    <a class="dropdown-item" href="#"><i :class="`fa-solid ${contact.icon}`"></i>
                                        {{ contact.number }}</a>
                                </li>

                            </ul>
                        </div>
                    </span> -->
                </div>

                <div>
                    <span>Call 24/7 . 800-8754-987</span>
                </div>
            </div>
        </div>
    </section>
</template>


<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins";


section {
    border-bottom: 1px solid rgba(255, 255, 255, 0.233);

    .btn {
        color: gray;

        &:hover {
            color: $color-secondary
        }
    }

    .divider {
        border-left: 1px solid rgba(255, 255, 255, 0.212);
        height: 10px;

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

    .dropdown-menu {
        @include mixins.dropdown-menu-default;

        .dropdown-item {
            @include mixins.dropdown-item-default;

            &:hover {
                color: $color-secondary;
            }
        }
    }

}

.dropdown-toggle {
    &:after {
        display: none;
    }
}
</style>