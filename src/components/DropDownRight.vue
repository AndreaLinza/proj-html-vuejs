<script>
import Search from './Search.vue';




export default {

    components: {
        Search,

    },


    data() {
        return {
            dropIcon: [

                'fa-magnifying-glass',
                'fa-solid fa-dragon',
                'fa-bag-shopping'

            ],
        }
    }

}

</script>

<template>
    <div class="nav-item dropdown dropdown-toggle px-3">
        <a class="nav-link" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            <i :class="`fa-solid ${dropIcon[0]}`"></i>
        </a>
        <ul class="dropdown-menu bg-transparent border-0 dropdown-menu-end dropdown-menu-lg-end">
            <li>
                <a class="dropdown-item d-flex" href="#">
                    <Search></Search>
                </a>
            </li>
        </ul>
    </div>
    <div class="nav-item dropdown dropdown-toggle px-3">
        <a class="nav-link" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            <i :class="`fa-solid ${dropIcon[1]}`"></i>
        </a>
        <ul class="dropdown-menu dropdown-menu-end dropdown-menu-lg-end">
            <li>
                <a class="dropdown-item" href="#">
                    <div class="d-flex flex-column">
                        <span class="py-1">User Login</span>
                        <span class="py-1">Checkout</span>
                    </div>
                </a>
            </li>

        </ul>
    </div>
    <div class="nav-item dropdown dropdown-toggle px-3">
        <a class="nav-link" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            <i :class="`fa-solid ${dropIcon[2]}`"></i> <span style="color:#F9AA01;">(0) £0.00</span>
        </a>
        <ul class="dropdown-menu dropdown-menu-end dropdown-menu-lg-end">
            <li>
                <a class="dropdown-item d-flex" href="#">
                    <span class="p-4">No products in the cart.</span>
                </a>
            </li>

        </ul>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixins";


.dropdown-menu {
    @include mixins.dropdown-menu-default;

    &.show{
        position: absolute;
        top:40px;
        border:1px solid rgba(255, 255, 255, 0.384)
    }

    .dropdown-item {
        @include mixins.dropdown-item-default;


    }
}

.nav-link {
    &:hover {
        color: $color-secondary
    }
}

.dropdown-toggle {
    &:after {
        display: none;
    }
}
</style>