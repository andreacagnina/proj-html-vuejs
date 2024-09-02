<script>
export default {
    props: {
        logo: {
            type: Object
        },
        PopularCourses: {
            type: Object
        },
        support: {
            type: Object
        },
    }
}
</script>

<template>
    <div class="container py-5 my-5 b-bottom">
        <div class="row">
            <div class="col-6 col-lg-3">
                <div class="content">
                    <h3 class="mb-5">
                        <img src="../../assets/img/logo-light.png" alt="logo" class="img-resize">
                    </h3>
                    <ul>
                        <li class="py-3 lh-lg" v-for="(label, index) in logo" :key="`logo-${index}`">
                            <a :href="label.url" v-html="label.label"></a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="col-6 col-lg-3">
                <div class="content">
                    <h3 class="mb-5">
                        Popular Courses
                    </h3>
                    <ul>
                        <li class="py-3 lh-lg" v-for="(label, index) in PopularCourses" :key="`courses-${index}`">
                            <p><a href="#">{{ label.matter }}</a></p>
                            <p><a href="#">{{ label.teacher }}</a></p>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="col-6 col-lg-3">
                <div class="content">
                    <h3 class="mb-5">
                        Support
                    </h3>
                    <ul>
                        <li class="py-3 lh-lg" v-for="(label, index) in support" :key="`support-${index}`">
                            <a :href="label.url" v-html="label.label"></a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="col-6 col-lg-3">
                <div class="content">
                    <h3 class="mb-5">
                        Flexible Learning
                    </h3>
                    <ul>
                        <li class="py-3 lh-lg">
                            <a href="#"><img src="../../assets/img/footer-img-1.png" alt="world map" class="w-100"></a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/Colors' as*;

a,
p {
    color: $cecece;

    &:hover {
        color: $ffffff;
    }
}

.img-resize {
    width: 200px;
}

.b-bottom {
    border-bottom: 1px solid $cecece;
}
</style>
