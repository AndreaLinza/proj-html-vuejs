<script>

export default {

    

}

</script>

<template>
    <div class="input-group d-flex">
        <input type="text" class="form-control" placeholder="Search products..." aria-label="Search products..."
            aria-describedby="button-addon2">
        <button class="btn btn-outline-secondary" type="button" id="button-addon2"><i
                class="fa-solid fa-magnifying-glass"></i></button>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

div{
    width: 300px;

    position: relative;
    top: -11px;

    .form-control{
        background-color: $color-primary;
        border-radius: 0;
        border-color: rgba(255, 255, 255, 0.384);

    }
    ::placeholder{
        color: white;
    }

    .btn{
        border-radius: 0;
        border-color: rgba(255, 255, 255, 0.384);
        border-left-color: transparent;
        background-color: $color-primary;

        &:hover{
            color: $color-secondary;
        }
    }
}


</style>