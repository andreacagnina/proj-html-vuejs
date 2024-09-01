<script>
export default {
    data() {
        return {
            accounts: [
                {
                    url: 'src/assets/img/h5-custom-icon-7.png',
                    title: 'Standard',
                    price: '$12',
                    package: [
                        {
                            courses: '2',
                            time: '15 Days',
                            wd: true,
                            hcd: true,
                            marketing: false,
                            python: false,
                            android: false,
                            english: false,
                        }
                    ]
                },
                {
                    url: 'src/assets/img/h5-custom-icon-8.png',
                    title: 'Professional',
                    price: '$59',
                    package: [
                        {
                            courses: '4',
                            time: '30 Days',
                            wd: true,
                            hcd: true,
                            marketing: true,
                            python: true,
                            android: false,
                            english: false,
                        }
                    ]
                },
                {
                    url: 'src/assets/img/h5-custom-icon-9.png',
                    title: 'Advanced',
                    price: '$88',
                    package: [{
                        courses: '6',
                        time: '30 Days',
                        wd: true,
                        hcd: true,
                        marketing: true,
                        python: true,
                        android: true,
                        english: true
                    }]
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
                        <table class="table table-bordered">
                            <thead>
                                <tr>
                                    <th scope="col">Save up to 40% by paying weekly</th>
                                    <th scope="col" v-for="account in accounts">
                                        <div class="text-center">
                                            <img :src="account.url" alt="">
                                            <div>{{
                                                account.title }}</div>
                                            <div>{{ account.price }}</div>
                                        </div>
                                    </th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td scope="row">Number of Courses</td>
                                    <td v-for="account in accounts">
                                    <td v-for="a in account.package"> {{ a.courses }}</td>
                                    </td>
                                </tr>
                                <tr>
                                    <td scope="row">Time</td>
                                    <td v-for="account in accounts">
                                    <td v-for="a in account.package"> {{ a.time }}</td>
                                    </td>
                                </tr>
                                <tr>
                                    <td scope="row">Web Designing</td>
                                    <td v-for="account in accounts">
                                    <td v-for="a in account.package"> {{ a.wd }}</td>
                                    </td>
                                </tr>
                                <tr>
                                    <td scope="row">Human-Centered Design</td>
                                    <td v-for="account in accounts">
                                    <td v-for="a in account.package"> {{ a.hcd }}</td>
                                    </td>
                                </tr>
                                <tr>
                                    <td scope="row">Basic Marketing</td>
                                    <td v-for="account in accounts">
                                    <td v-for="a in account.package"> {{ a.marketing }}</td>
                                    </td>
                                </tr>
                                <tr>
                                    <td scope="row">Python for Everybody</td>
                                    <td v-for="account in accounts">
                                    <td v-for="a in account.package"> {{ a.python }}</td>
                                    </td>
                                </tr>
                                <tr>
                                    <td scope="row"> Android Developer</td>
                                    <td v-for="account in accounts">
                                    <td v-for="a in account.package"> {{ a.android }}</td>
                                    </td>
                                </tr>
                                <tr>
                                    <td scope="row">Business</td>
                                    <td v-for="account in accounts">
                                    <td v-for="a in account.package"> {{ a.english ? 'ok' : 'ko' }}</td>
                                    </td>
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

tr {
    text-align: center;
}
</style>