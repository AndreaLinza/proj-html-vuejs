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
    <section class="py-1">
        <div class="container">
            <div class="d-flex justify-content-between">
                <div class="d-flex align-items-center">
                    <span class="mx-2">
                        <small>
                            Wishlist (0)
                        </small>
                    </span>
                    <span class="divider"></span>
                    <span class="btn-group d-flex">
                        <button class="btn dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
                            <small>
                                Need Help ?
                            </small>
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
                </div>

                <div class="pt-2">
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

    span {
        color: rgba(255, 255, 255, 0.623);

        &:hover {
            color: $color-secondary
        }

        i {
            font-size: 10px;
            padding: 0 .5rem;

        }
    }

    .btn {
        color: rgba(255, 255, 255, 0.623);
        border: 0;

        &:hover {
            color: $color-secondary
        }
    }

    .divider {
        border-left: 1px solid rgba(255, 255, 255, 0.281);
        height: 13px; 

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