<script>

import HJumbotronCarouselSection from './HJumbotronCarouselSection.vue';

export default {
    components: {
        HJumbotronCarouselSection,
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
    <div class="carousel-container position-relative">
        <div class="carousel-slide" v-for="(slide, index) in slides" :key="index" v-show="(index === currentIndex)">
            <img :src="slide" alt="carousel image" />
            <HJumbotronCarouselSection />
        </div>
        <div class=" carousel-indicators">
            <span v-for="(slide, index) in slides" :key="index" @click="goToSlide(index)"><i
                    :class="(index === currentIndex) ? 'fa-regular fa-circle-dot fa-xl active' : 'fa-solid fa-circle fa-xl'"></i></span>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/Colors' as*;



.carousel-container {
    width: 100%;
}

.carousel-slide {
    width: 100%;
    height: 100vh;
}



.carousel-slide img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.carousel-indicators {
    position: absolute;


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