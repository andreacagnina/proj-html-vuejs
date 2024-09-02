<script>
export default {

}
</script>

<template>
    <div
        class="container carousel-caption position-absolute start-50 translate-middle lh-lg d-flex align-items-center justify-content-center">
        <div class="row">
            <div class="col-12">
                <div class="content">
                    <h1 class="mb-4 d-none d-lg-block">Contemporary Ideas</h1>
                    <p class="d-none d-lg-block"> Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis
                        recusandae
                        eligendi nulla
                        reiciendis, repudiandae fugit? Numquam deserunt maiores nihil at possimus, repudiandae quae,
                        nisi ab
                        animi accusantium sunt iste ad.</p>
                    <button class="button mt-5" data-bs-toggle="offcanvas" data-bs-target="#offcanvasRight"
                        aria-controls="offcanvasRight">REGISTER NOW</button>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/Colors' as*;

h1 {
    font-weight: 600;
}

.button {
    background-color: $a40c4ff;
    border: $a000000;
    color: $ffffff;
    padding: 20px 60px;
    font-weight: 600;

    &:hover {
        background-color: $a9ce0ff;
        text-shadow: 2px 2px 4px #000000;
        transition-duration: 0.4s;
    }
}
</style>