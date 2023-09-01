<script>
import Search from './Search.vue';



export default {

    components: {
        Search,
    },


    props: {

        dropIcon: {
            type: String,
            required: true
        },

        dropLink: {
            type: Array,
            required: true,

        }
    }




}

</script>

<template>
    <div class="nav-item dropdown dropdown-toggle"
    v-for="icon in dropIcon">
        <a class="nav-link" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false" >
            <i :class="`fa-solid ${icon}`"></i>
            
        </a>
        <ul class="dropdown-menu dropdown-menu-end dropdown-menu-lg-end">
            <li><a class="dropdown-item d-flex" href="#">
                    <Search></Search>

                </a></li>

        </ul>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.dropdown-menu {
    background-color: black;
    border-radius: 0;


    .dropdown-item {
        background-color: transparent;
        color: white;
        width: auto;

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