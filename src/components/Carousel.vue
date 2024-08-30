<script>
export default {
    data() {
        return {
            slides: [
                '/src/assets/img/h5-slide-1-background.jpg',
                '/src/assets/img/h5-slide-2-background.jpg',
                '/src/assets/img/h5-slide-3-background.jpg',
            ]
        }
    }
}
</script>

<template>
    <div class="carousel-container">
        <div class="carousel-slide" v-for="(slide, index) in slides" :key="index">
            <img :src="slide" alt="carousel image" />
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/bgColors' as*;
@use '../styles/partials/borderColors' as*;
@use '../styles/partials/fillColors' as*;
@use '../styles/partials/textColors' as*;
</style>