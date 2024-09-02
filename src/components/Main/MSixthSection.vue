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
                            <h1>Pricing Plans</h1>
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
                        <div class="content">
                            <table class="table table-borderless">
                                <thead>
                                    <tr>
                                        <th scope="col" class="bord-top w-350">
                                            <h3>Save up to 40% <br>by
                                                paying weekly</h3>
                                        </th>
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
                                        <td scope="row" class="l-bold">Number of Courses</td>
                                        <td v-for="account in accounts">
                                            {{ account.courses }}
                                        </td>
                                    </tr>
                                    <tr>
                                        <td scope="row" class="l-bold">Time</td>
                                        <td v-for="account in accounts">
                                            {{ account.time }}
                                        </td>
                                    </tr>
                                    <tr>
                                        <td scope="row" class="l-bold">Web Designing</td>
                                        <td v-for="account in accounts" :class="getAccountClass(account, 'wd')">
                                            {{ getAccountSymbol(account, 'wd') }}
                                        </td>
                                    </tr>
                                    <tr>
                                        <td scope="row" class="l-bold">Human-Centered Design</td>
                                        <td v-for="account in accounts" :class="getAccountClass(account, 'hcd')">
                                            {{ getAccountSymbol(account, 'hcd') }}
                                        </td>
                                    </tr>
                                    <tr>
                                        <td scope="row" class="l-bold">Basic Marketing</td>
                                        <td v-for="account in accounts" :class="getAccountClass(account, 'marketing')">
                                            {{ getAccountSymbol(account, 'marketing') }}
                                        </td>
                                    </tr>
                                    <tr>
                                        <td scope="row" class="l-bold">Python for Everybody</td>
                                        <td v-for="account in accounts" :class="getAccountClass(account, 'python')">
                                            {{ getAccountSymbol(account, 'python') }}
                                        </td>
                                    </tr>
                                    <tr>
                                        <td scope="row" class="l-bold"> Android Developer</td>
                                        <td v-for="account in accounts" :class="getAccountClass(account, 'android')">
                                            {{ getAccountSymbol(account, 'android') }}
                                        </td>
                                    </tr>
                                    <tr>
                                        <td scope="row" class="l-bold">Business</td>
                                        <td v-for="account in accounts" :class="getAccountClass(account, 'english')">
                                            {{ getAccountSymbol(account, 'english') }}
                                        </td>
                                    </tr>
                                    <tr>
                                        <td class="invisible no-border"></td>
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

h2,
h3,
h4,
h5,
h6 {
    font-weight: 600;
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

.bord-top {
    border-top: 7px solid $a9ce0ff;
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

.no-border {
    border-left: 1px solid rgba(0, 0, 0, 0);
    border-bottom: 1px solid rgba(0, 0, 0, 0);
}

.l-bold {
    text-align: left;
    font-weight: 600;
    padding: 20px 50px;
    color: $a847b7b;
}

.w-350 {
    width: 350px;
}
</style>