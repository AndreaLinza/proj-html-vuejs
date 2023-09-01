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
    <div class="nav-item dropdown dropdown-toggle px-4">
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
    <div class="nav-item dropdown dropdown-toggle px-4">
        <a class="nav-link" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            <i :class="`fa-solid ${dropIcon[1]}`"></i>
        </a>
        <ul class="dropdown-menu dropdown-menu-end dropdown-menu-lg-end">
            <li>
                <a class="dropdown-item d-flex" href="#">
                </a>
            </li>

        </ul>
    </div>
    <div class="nav-item dropdown dropdown-toggle px-4">
        <a class="nav-link" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            <i :class="`fa-solid ${dropIcon[2]}`"></i>
        </a>
        <ul class="dropdown-menu dropdown-menu-end dropdown-menu-lg-end">
            <li>
                <a class="dropdown-item d-flex" href="#">

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
    .dropdown-item {
        @include mixins.dropdown-item-default;
    }
}
.nav-link{
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