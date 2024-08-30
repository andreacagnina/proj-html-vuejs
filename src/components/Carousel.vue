<script>

import CarouselSection from './CarouselSection.vue';

export default {
    components: {
        CarouselSection,
    },
    data() {
        return {
            slides: [
                '/src/assets/img/h5-slide-1-background.jpg',
                '/src/assets/img/h5-slide-2-background.jpg',
                '/src/assets/img/h5-slide-3-background.jpg',
            ],
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
    <div class="carousel-container">
        <div class="carousel-slide" v-for="(slide, index) in slides" :key="index"
            :class="(index === currentIndex) ? 'active' : ''">
            <img :src="slide" alt="carousel image" />
            <CarouselSection />
        </div>
        <div class=" carousel-indicators">
            <span v-for="(slide, index) in slides" :key="index" @click="goToSlide(index)"><i
                    :class="(index === currentIndex) ? 'fa-regular fa-circle-dot fa-xl active' : 'fa-solid fa-circle fa-xl'"></i></span>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/Colors' as*;



.carousel-container {
    position: relative;
    width: 100%;
}

.carousel-slide {
    width: 100%;
    height: 100vh;
    display: none;
}

.carousel-slide.active {
    display: block;
}

.carousel-slide img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.carousel-indicators {
    position: absolute;
    //bottom: 30px;

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

}
</style>