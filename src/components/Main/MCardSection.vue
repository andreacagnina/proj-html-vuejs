<script>

export default {
    data() {
        return {
            matterCards: [
                {
                    title: 'Languages',
                    url: '/src/assets/img/h5-custom-icon-1.png',
                },
                {
                    title: 'Software',
                    url: '/src/assets/img/h5-custom-icon-2.png',
                },
                {
                    title: 'Business',
                    url: '/src/assets/img/h5-custom-icon-3.png',
                },
                {
                    title: 'Chemistry',
                    url: '/src/assets/img/h5-custom-icon-4.png',
                },
                {
                    title: 'Science',
                    url: '/src/assets/img/h5-custom-icon-5.png',
                },
                {
                    title: 'DIY&Craft',
                    url: '/src/assets/img/h5-custom-icon-6.png',
                },
            ]
        }
    }

}
</script>

<template>
    <section>
        <div class="container my-5">
            <div class="row">
                <div class="col-6 col-md-4 g-2 col-lg-2" v-for="(card, index) in matterCards" :key="`card-${index}`">
                    <a href="#">
                        <div class="content matter-card p-5 p-md-2">
                            <img :src="card.url" alt="img matter">
                            <h4>{{ card.title }}</h4>
                        </div>
                    </a>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/Colors' as*;

a {
    color: $a000000;
}

.matter-card {
    border: 1px solid $f2f2f2;
    background-color: $fcfcfc;
    text-align: center;
    cursor: pointer;

    &:hover {
        border: 1px solid $a40c4ff;
        transition-duration: 0.4s;
    }

    h4 {
        margin-top: 2rem;
    }

}
</style>