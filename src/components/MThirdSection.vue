<script>
import Avatar from './Avatar.vue';
import { Testimonials } from '../data/Testimonials';


export default {
    components: {
        Avatar,
    },
    data() {
        return {
            Testimonials,
            currentIndex: 0,
        }
    },
}

</script>

<template>
    <div class="container-fluid position-relative">
        <div class="row">
            <div class="col-12">
                <div class="content position-absolute top-50 start-50 translate-middle text-center">
                    <Avatar :Testimonials="Testimonials" />
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/Colors' as*;

.container-fluid {
    background-image: url(../assets/img/interactive-map-slider-img-1.png);
    background-repeat: no-repeat;
    background-position: 30% 400px;
    background-color: $a40c4ff;
    background-size: cover;
    height: 100vh;

}
</style>