<script>
export default {
    data() {
        return {
            brands: [{
                picstatic:
                    '/src/assets/img/h5-client-5.png',
                picdinamic:
                    '/src/assets/img/h5-client-5-h.png',
                hover: false,
            }, {
                picstatic:
                    '/src/assets/img/h5-client-1.png',
                picdinamic:
                    '/src/assets/img/h5-client-1-h.png',
                hover: false,
            }, {
                picstatic:
                    '/src/assets/img/h5-client-2.png',
                picdinamic:
                    '/src/assets/img/h5-client-2-h.png',
                hover: false,
            }, {
                picstatic:
                    '/src/assets/img/h5-client-1.png',
                picdinamic:
                    '/src/assets/img/h5-client-1-h.png',
                hover: false,
            }
            ],
        }
    },
}
</script>

<template>
    <section>
        <div class="container py-5">
            <div class="row">
                <div class="col-3" v-for="(brand, index) in brands" key="index">
                    <div class="content py-5">
                        <img :src="(brand.hover == false) ? `${brand.picstatic}` : `${brand.picdinamic}`"
                            alt="logo brand" @mouseover="brand.hover = true" @mouseleave="brand.hover = false">
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/Colors' as*;

.content {
    cursor: pointer;
}
</style>