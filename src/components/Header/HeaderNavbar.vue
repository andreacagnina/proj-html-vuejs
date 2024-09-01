<script>
export default {
    props: {
        navMenu: {
            type: Object
        },
    }
}
</script>

<template>

    <nav class="navbar navbar-expand-lg">
        <div class="container">
            <div class="navbar-brand">
                <a href="#">
                    <img src="../../assets/img/logo-light.png" alt="logo">
                </a>
            </div>
            <div class="collapse navbar-collapse order-3" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item" v-for="(label, index) in navMenu" :key="`HM-${index}`">
                        <a class="nav-link" :href="label.url">{{
                            label.label }}</a>
                    </li>
                </ul>
            </div>
            <div class="order-2 order-lg-3">
                <ul class="navbar-nav flex-row order-2">
                    <li class="">
                        <a href="#" class="nav-link"><i class="fa-solid fa-magnifying-glass fa-rotate-90 fa-xl"></i></a>
                    </li>
                    <li class="nav-item">
                        <a href="#" class="nav-link"><i class="fa-solid fa-bag-shopping fa-xl position-relative"><span
                                    class="position-absolute bottom-100 start-50 badge rounded-pill bg-badge fs-6">
                                    0</span></i></a>
                    </li>
                    <li class="nav-item d-lg-none">
                        <button class="nav-link" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                            aria-expanded="false">
                            <i class="fa-solid fa-bars fa-xl" style="color: white;"></i>
                        </button>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/Colors' as*;

img {
    width: 250px;
}


ul {

    li {
        align-items: center;
        margin: 0 20px;
    }

    a {
        text-transform: uppercase;
        color: $ffffff;
    }
}


.bg-badge {
    background-color: $a40c4ff;
}
</style>