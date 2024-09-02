<script>
export default {
    data() {
        return {
            cards: [
                {
                    url: 'src/assets/img/course-5-f-img.jpg',
                    title: 'Android Developer',
                    teacher: 'David Sanders',
                    category: 'PROGRAMMING',
                    numOfTeacher: '1',
                    price: 'FREE',

                },
                {
                    url: 'src/assets/img/course-6-f-img.jpg',
                    title: 'Web Designing',
                    teacher: 'Jennifer Powell',
                    category: 'PROGRAMMING',
                    numOfTeacher: '1',
                    price: 'FREE',

                },
                {
                    url: 'src/assets/img/course-12-f-img.jpg',
                    title: 'Financial Modeling',
                    teacher: 'Edward Bowman',
                    category: 'BUSINESS',
                    numOfTeacher: '1',
                    price: '$20',
                },
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
    <section id="2">
        <div class="container-fluid bg-img py-5 border">
            <div class="container">
                <div class="row">
                    <div class="col-12">
                        <div class="content text-center py-5">
                            <h2>Popular Online Courses</h2>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. A reprehenderit ipsa
                                consequuntur
                                enim
                                maiores amet cupiditate hic fugiat laudantium veritatis? Non id pariatur velit enim
                                laborum
                                nihil, quo illo reiciendis?</p>
                        </div>
                    </div>
                </div>
                <div class="row">
                    <div class="col-12 col-md-4" v-for="(card, index) in cards" :key="index">
                        <div class="content py-3 py-md-5">
                            <div class="card">
                                <img :src="card.url" class="card-img-top" alt="card img">
                                <div class="card-body pb-0 d-flex justify-content-between align-items-center">
                                    <h4 class="card-title">{{ card.teacher }}</h4>
                                    <span class="badge rounded-pill text-white"
                                        :class="(card.price === 'FREE') ? 'free' : 'payment'">{{ card.price
                                        }}</span>
                                </div>
                                <div class="card-body pt-0">
                                    <h5 class="card-title">{{ card.teacher }}</h5>
                                    <p class="card-text my-4">Lorem ipsum dolor sit amet consectetur adipisicing elit.
                                        Laborum
                                        officiis aliquam cum eos, ullam nam labore fuga iste sapiente minus nulla at,
                                        voluptate
                                        illum deserunt possimus corrupti non deleniti suscipit!</p>
                                    <p class="card-text"><small class="text-body-secondary"><i
                                                class="fa-solid fa-user"></i>&nbsp;&nbsp;<span>{{ card.numOfTeacher
                                                }}</span>&nbsp;&nbsp;<i class="fa-solid fa-tag"></i>&nbsp;&nbsp;<span
                                                class="fw-bold">{{
                                                    card.category }}</span></small>
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="row">
                    <div class="col-12">
                        <div class="content text-center">
                            <div class="my-5">
                                <span v-for="(card, index) in cards" :key="index" @click="goToSlide(index)"><i
                                        :class="(index === currentIndex) ? 'fa-solid fa-circle active' : 'fa-solid fa-circle'"></i></span>
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

.bg-img {
    background-image: url(../../assets/img/page-background-img.png);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: 0% 30px;
}

p {
    color: $a847b7b;
}

h5,
span {
    color: $a847b7b;
}

.free {
    background-color: $ffd740;
}

.payment {
    background-color: $a40c4ff;
}

span {
    i {
        padding: 10px;
        cursor: pointer;
        color: $a9ce0ff;
    }
}

.active {
    color: $a40c4ff;
}

.badge {
    width: 70px;

}

.pt-0 {
    padding-top: 0;
}

.pb-0 {
    padding-bottom: 0;
}
</style>