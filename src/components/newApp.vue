<script>
export default {

}
</script>

<template>
    <div>

    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/Colors' as*;
</style>

<div class="d-flex">
    <div class="card" style="width: 18rem;" v-for="account in accounts">
        <ul class="list-group list-group-flush" v-for="a in account.package">
            <li class="list-group-item" v-for="b in a">{{ a.courses }}</li>

        </ul>
    </div>
</div>

{

title: 'Save up to 40% by paying weekly',
price: '$12',
package: [
{
courses: 'Number of Courses',
time: 'Time',
wd: 'Web Designing',
hcd: 'Human-Centered Design',
marketing: 'Basic Marketing',
python: 'Python for Everybody',
android: 'Android Developer',
english: 'Business',
}
]
},