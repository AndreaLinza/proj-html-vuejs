<script>



export default {

    data() {
        return {

            navLinks: [
                'Home',
                'Shop',
                'Blog',
                'Media',
                'ShortCode',
                'Feature',
            ],




        }
    },


}

</script>


<template>
    <div class="list-group">
        <li class="d-flex">
            <a href="#" class="list-group-item list-group-item-action" aria-current="true" 
            v-for="navLink in navLinks">
                {{ navLink }}
            </a>
        </li>
    </div>
</template>


<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;

.list-group {
    .list-group-item {
        @include list-item-default;

        padding: 0 1.2rem;
        color: $color-text;

        &:hover {
            color: $color-secondary;

        }


        &:hover {
            @include list-item-action
        }

        &:focus {
            @include list-item-action
        }
    }

    .btn {
        background-color: transparent;
        border: 0;

        &:hover {
            @include list-item-action
        }
    }

    .dropdown-toggle {

        &:after {
            display: none;
        }
    }
}
</style>