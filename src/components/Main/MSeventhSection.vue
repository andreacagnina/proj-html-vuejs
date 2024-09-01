<script>
export default {
    data() {
        return {
            brands: [
                '/src/assets/img/h5-client-5.png',
                '/src/assets/img/h5-client-1.png',
                '/src/assets/img/h5-client-2.png',
                '/src/assets/img/h5-client-1.png',
            ],
            brandsHover: [

            ],
        }
    },
}
</script>

<template>
    <div class="container py-5">
        <div class="row">
            <div class="col-3" v-for="(brand, index) in brands">
                <div class="content py-5">
                    <img :src="brand" alt="">
                    <img src="" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/Colors' as*;

</style>