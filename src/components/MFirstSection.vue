<script>
export default {

}
</script>

<template>
    <div class="container">
        <div class="row">
            <div class="col-12 col-md-5">
                <div class="content">
                    <h2 class="text-capitalize">the trusted name for in-home tutoring.</h2>
                </div>
            </div>
            <div class="col-12">
                <div class="content">
                    <p class="my-3">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Facilis nostrum
                        consequatur veritatis
                        doloribus, ullam iure saepe officiis cum numquam corporis animi aspernatur sint eius tenetur
                        minima! At expedita maiores ea.</p>
                    <a href="#">
                        <h3 class="lead text-uppercase">learn more</h3>
                    </a>
                </div>
            </div>
            <div class="col-12">
                <div class="content">
                    <img src="../assets/img/h5-img-1.jpg" alt="img">
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/Colors' as*;

h2,
h3 {
    font-weight: 600;
}

p {
    color: $a847b7b;
}

h3 {
    color: $a40c4ff;
}

img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>