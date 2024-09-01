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
    <div class="container-fluid bg-img py-5 border">
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="content text-center py-5">
                        <h1>Pricing Plans</h1>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. A reprehenderit ipsa consequuntur
                            enim
                            maiores amet cupiditate hic fugiat laudantium veritatis? Non id pariatur velit enim laborum
                            nihil, quo illo reiciendis?</p>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col-12">
                    <div class="content">
                        <table class="table border">
                            <thead>
                                <tr>
                                    <th scope="col">Save up to 40% by paying weekly</th>
                                    <th scope="col">First</th>
                                    <th scope="col">Last</th>
                                    <th scope="col">Handle</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <th scope="row">1</th>
                                    <td>Mark</td>
                                    <td>Otto</td>
                                    <td>@mdo</td>
                                </tr>
                                <tr>
                                    <th scope="row">2</th>
                                    <td>Jacob</td>
                                    <td>Thornton</td>
                                    <td>@fat</td>
                                </tr>
                                <tr>
                                    <th scope="row">3</th>
                                    <td colspan="2">Larry the Bird</td>
                                    <td>@twitter</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/Colors' as*;

.bg-img {
    background-image: url(../../assets/img/page-background-img.png);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: 0% 200px;
}

h2,
h3,
h4,
h5,
h6 {
    font-weight: 600;
}

/*p {
    color: $a847b7b;
}
    */



.active {
    color: $a40c4ff;
}
</style>