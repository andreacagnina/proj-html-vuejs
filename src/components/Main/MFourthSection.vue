<script>
export default {
    data() {
        return {
            infos: [
                'What We Do',
                'Degree Programme',
                'Career Achievements',
                'Personal Management',
                'Steps To Success',
                'Knowledge Transfer',
            ],
            labels: [
                'We enrich lives through learning.',
                'Maximizing potential through individual attention.',
                'The trusted name for specialized training.',
                'People teach. People learn. This where thy connect.',
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
    <section>
        <div class="container my-5">
            <div class="row">
                <div class="col-12 col-md-4">
                    <div class="content my-5">
                        <div>
                            <ul class="list-group">
                                <li class="list-group-item" v-for="(tab, index) in infos" :key="index"
                                    @click="goToSlide(index)" :class="{ 'selected': (index === currentIndex) }">{{
                                        tab }}</li>
                                <!-- <li class="list-group-item" v-for="(tab, index) in infos" :key="index"
                                    @click="goToSlide(index)" :class="(index === currentIndex) ? 'selected' : ''">{{
                                        tab }}</li> -->
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="col-12 col-md-8">
                    <div class="content my-md-5 py-4 ps-5">
                        <h2>Learning Possibilities</h2>
                        <p class="mt-4 mb-5">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate,
                            obcaecati,
                            deserunt
                            explicabo corrupti vitae aut tenetur sunt a ipsam velit voluptates quo aliquid et,
                            reiciendis
                            ipsa ex voluptatibus minima nulla.</p>
                        <div class="row">
                            <div class="col-8">
                                <div class="content">
                                    <ul class="lh-lg py-md-5">
                                        <li class="py-2" v-for="(label, index) in labels" :key="index">
                                            <span><i class="fas fa-check"></i>&nbsp;</span><span>{{ label }}</span>
                                        </li>
                                    </ul>
                                </div>
                            </div>
                            <div class="col-4 align-self-end">
                                <div class="content ">
                                    <img src="../../assets/img/h12-tabs-icon-1.png" alt="geom img">
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

</template>

<style lang="scss" scoped>
@use '../../styles/partials/Colors' as*;

ul.list-group {
    li {
        font-weight: 600;
        color: $a847b7b;
        padding: 30px 40px;

    }

    li:hover {
        color: $a55acee;
        background-color: $fcfcfc;
        cursor: pointer;
    }

    .selected {
        color: $a40c4ff;
        background-color: $fcfcfc;
        border-left: 10px solid $a40c4ff;
    }
}

i {
    color: $a40c4ff;
}

p {
    color: $a847b7b;
}

.col-8 li {

    color: $a847b7b;

}
</style>
