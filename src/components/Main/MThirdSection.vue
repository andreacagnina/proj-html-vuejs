<script>
export default {
    data() {
        return {
            Testimonials: [
                {
                    url: '/src/assets/img/instructor-img-6-150x150.jpg',
                    cit: '"Mroin gravida nibh vel leiuctor aliquenean sollicitudin, lorem quis bibendum auctor, nisi elit consequat ipsutis sem nibh id elit. Duis sed odio sit amet nibulputate cursus a sit amet mauris. Morbi accumsan ipsum velit. Nam nec tellus."',
                    name: 'Joan Collins',
                    role: 'Student'
                },
                {
                    url: '/src/assets/img/instructor-img-8-150x150.jpg',
                    cit: '"Mroin gravida nibh vel leiuctor aliquenean sollicitudin, lorem quis bibendum auctor, nisi elit consequat ipsutis sem nibh id elit. Duis sed odio sit amet nibulputate cursus a sit amet mauris. Morbi accumsan ipsum velit. Nam nec tellus."',
                    name: 'XXX',
                    role: 'Scientist'
                },
                {
                    url: '/src/assets/img/instructor-img-4-150x150.jpg',
                    cit: '"Mroin gravida nibh vel leiuctor aliquenean sollicitudin, lorem quis bibendum auctor, nisi elit consequat ipsutis sem nibh id elit. Duis sed odio sit amet nibulputate cursus a sit amet mauris. Morbi accumsan ipsum velit. Nam nec tellus."',
                    name: 'XXX',
                    role: 'Teacher'
                },],

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
                <div class="content">
                    <div v-show="index === currentIndex" v-for="(testimonial, index) in Testimonials" :key="index"
                        class="position-absolute top-50 start-50 translate-middle text-center">
                        <div class="avatar p-3">
                            <img :src="testimonial.url" alt="Avatar" class="mb-3">
                        </div>
                        <p class="my-5 lh-base d-none d-lg-inline">{{ testimonial.cit }}</p>
                        <h3 class="mt-5 mb-4">{{ testimonial.name }}</h3>
                        <h5 class="text-uppercase">{{ testimonial.role }}</h5>
                    </div>
                    <div class="position-absolute-ind my-5">
                        <span v-for="(testimonial, index) in Testimonials" :key="index" @click="goToSlide(index)"><i
                                :class="(index === currentIndex) ? 'fa-solid fa-circle active' : 'fa-solid fa-circle'"></i></span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/Colors' as*;

.container-fluid {
    background-image: url(../../assets/img/interactive-map-slider-img-1.png);
    background-repeat: no-repeat;
    background-position: 30% 370px;
    background-color: $a40c4ff;
    background-size: cover;
    height: 900px;
}

.position-absolute-ind {
    position: absolute;
    bottom: 100px;
    right: 50%;
    transform: translate(50%);
}

.avatar {
    margin: 0 auto;

    img {
        width: 150px;
        border-radius: 50%;
        object-fit: fill;
    }
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
h3,
h5 {
    font-weight: 600;
}

p,
h2,
h3,
h5 {
    color: $ffffff;
    ;
}
</style>