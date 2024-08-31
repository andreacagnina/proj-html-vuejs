<script>

import { Testimonials } from '../data/Testimonials';


export default {
    data() {
        return {
            Testimonials,
            currentIndex: 0,
        }
    },
    methods: {
        goToSlide(index) {
            this.currentIndex = index;
        }
    },
}

</script>

<template>
    <div class="container-fluid position-relative">
        <div class="row">
            <div class="col-12">
                <div class="content position-absolute top-50 start-50 translate-middle text-center">
                    <div class="test-slider" :class="(index === currentIndex) ? 'active' : ''"
                        v-for="(testimonial, index) in Testimonials" :key="index">
                        <img :src="testimonial.url" alt="Avatar" class="avatar mb-3 d-none d-md-inline-block">
                        <p class="my-5 lh-lg">{{ testimonial.cit }}</p>
                        <h3>{{ testimonial.name }}</h3>
                        <h5 class="text-uppercase my-3">{{ testimonial.role }}</h5>
                    </div>
                    <div class="slides-indicators my-5">
                        <span v-for="(testimonial, index) in Testimonials" :key="index" @click="goToSlide(index)"><i
                                :class="(index === currentIndex) ? 'fa-solid fa-circle active' : 'fa-solid fa-circle'"></i></span>
                    </div>
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

.avatar {
    vertical-align: middle;
    width: 200px;
    height: 200px;
    border-radius: 50%;
    object-fit: cover;
}

.test-slider {
    display: none;
}

.test-slider.active {
    display: block;
}


span {
    padding: 10px;

    i {
        cursor: pointer;
        color: $ffffff4d;
    }
}

.active {
    color: $ffffff;
}

h2,
h3 {
    font-weight: 600;
}
</style>