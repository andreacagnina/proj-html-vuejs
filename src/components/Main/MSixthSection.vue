<script>
export default {
    data() {
        return {
            accounts: [
                {
                    url: 'src/assets/img/h5-custom-icon-7.png',
                    title: 'Standard',
                    price: '$12',
                    courses: '2',
                    time: '15 Days',
                    wd: true,
                    hcd: true,
                    marketing: false,
                    python: false,
                    android: false,
                    english: false,
                    borderClass: 'border-blue',

                },
                {
                    url: 'src/assets/img/h5-custom-icon-8.png',
                    title: 'Professional',
                    price: '$59',
                    courses: '4',
                    time: '30 Days',
                    wd: true,
                    hcd: true,
                    marketing: true,
                    python: true,
                    android: false,
                    english: false,
                    borderClass: 'border-blue',
                },
                {
                    url: 'src/assets/img/h5-custom-icon-9.png',
                    title: 'Advanced',
                    price: '$88',
                    courses: '6',
                    time: '30 Days',
                    wd: true,
                    hcd: true,
                    marketing: true,
                    python: true,
                    android: true,
                    english: true,
                    borderClass: 'border-blue',
                },
            ],
        }
    },
    methods: {
        getAccountSymbol(account, key) {
            return account[key] ? '✔' : '✖';
        },
        getAccountClass(account, key) {
            return account[key] ? 'yes' : 'no';
        },
        changeBorderColor(index) {
            this.accounts.forEach((account) => {
                account.borderClass = 'border-blue';
            });
            const account = this.accounts[index];
            account.borderClass = 'border-selected';
        },
    }
}
</script>

<template>
    <section>
        <div class="container-fluid bg-img py-5 border">
            <div class="container">
                <div class="row">
                    <div class="col-12">
                        <div class="content text-center py-5">
                            <h2>Pricing Plans</h2>
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
                    <div class="col-12">
                        <div class="content table-responsive d-flex">
                            <div class="w-450">
                                <ul>
                                    <li class="pt-5 pb-3 ">
                                        <div class="py-4"></div>
                                        <h3>Save up to 40% <br>by
                                            paying weekly</h3>
                                    </li>
                                    <li>Number of Courses</li>
                                    <li>Time</li>
                                    <li>Web Designing</li>
                                    <li>Human-Centered Design</li>
                                    <li>Basic Marketing</li>
                                    <li>Python for Everybody</li>
                                    <li>Android Developer</li>
                                    <li>Business</li>
                                </ul>
                            </div>
                            <table class="table table-borderless ">

                                <thead>
                                    <tr>

                                        <th scope="col" v-for="(account, index) in accounts" :key="`sel-${index}`"
                                            :class="account.borderClass" class="bg-col">
                                            <div class="text-center">
                                                <img :src="account.url" alt="">
                                                <div class="my-2">
                                                    <h3>{{
                                                        account.title }}</h3>
                                                </div>
                                                <div>
                                                    <h3>{{ account.price }}</h3>
                                                </div>
                                            </div>
                                        </th>
                                    </tr>
                                </thead>
                                <tbody>
                                    <tr>
                                        <td v-for="account in accounts" class="no">
                                            {{ account.courses }}
                                        </td>
                                    </tr>
                                    <tr>
                                        <td v-for="account in accounts" class="no">
                                            {{ account.time }}
                                        </td>
                                    </tr>
                                    <tr>

                                        <td v-for="account in accounts" :class="getAccountClass(account, 'wd')">
                                            {{ getAccountSymbol(account, 'wd') }}
                                        </td>
                                    </tr>
                                    <tr>

                                        <td v-for="account in accounts" :class="getAccountClass(account, 'hcd')">
                                            {{ getAccountSymbol(account, 'hcd') }}
                                        </td>
                                    </tr>
                                    <tr>

                                        <td v-for="account in accounts" :class="getAccountClass(account, 'marketing')">
                                            {{ getAccountSymbol(account, 'marketing') }}
                                        </td>
                                    </tr>
                                    <tr>

                                        <td v-for="account in accounts" :class="getAccountClass(account, 'python')">
                                            {{ getAccountSymbol(account, 'python') }}
                                        </td>
                                    </tr>
                                    <tr>

                                        <td v-for="account in accounts" :class="getAccountClass(account, 'android')">
                                            {{ getAccountSymbol(account, 'android') }}
                                        </td>
                                    </tr>
                                    <tr>

                                        <td v-for="account in accounts" :class="getAccountClass(account, 'english')">
                                            {{ getAccountSymbol(account, 'english') }}
                                        </td>
                                    </tr>
                                    <tr>

                                        <td v-for="(account, index) in accounts" :key="`sel-${index}`" class="bg-col">
                                            <button class="button my-4" @click="changeBorderColor(index)">GET IT
                                                NOW</button>
                                        </td>
                                    </tr>
                                </tbody>
                            </table>

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
    background-position: 0% 200px;
}

tr {
    text-align: center;
}

.yes {
    color: $a40c4ff;
    font-weight: 600;
}

.no {
    color: $a847b7b;
}

.button {
    background-color: $ffffff;
    border: 2px solid $f2f2f2;
    color: $a847b7b;
    padding: 20px 50px;
    font-size: medium;
    font-weight: 600;

    &:hover {
        background-color: $a40c4ff;
        color: $ffffff;
        text-shadow: 2px 2px 4px #000000;
        transition-duration: 0.4s;

    }
}

.bg-col {
    background-color: $fcfcfc;

}

.border-blue {
    border-top: 7px solid $a9ce0ff;
}

.border-selected {
    border-top: 7px solid $a40c4ff;
}

th,
td,
tr {
    border: 1px solid $f2f2f2;
}

div.border li {
    border: 1px solid $f2f2f2;
    padding: 16px 50px;
    font-size: 1.2rem;
    font-weight: 600;
    color: $a847b7b;
    background-color: $ffffff;

    &:first-child {
        color: black;
        border-top: none;
    }
}

td.yes,
td.no {
    padding: 16px 50px
}

.w-450 {
    width: 450px;
    border-top: 7px solid $a9ce0ff;
}
</style>