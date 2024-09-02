<script>
export default {

}
</script>

<template>
    <section>
        <div class="container my-5 p-5">
            <div class="row align-items-center">
                <div class="col-12 col-lg-7">
                    <div class="content text-center">
                        <img src="../../assets/img/h1-img-8.jpg" alt="World img">
                        <!-- MANCA IMG NUVOLA -->
                    </div>
                </div>
                <div class="col col-lg-4">
                    <div class="content mt-3">
                        <h2 class="text-capitalize">empowering children to reach their potential.</h2>

                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Laborum quidem perspiciatis ea quas
                            animi placeat aspernatur. Odit veniam, ea rerum dolores similique vero harum quos hic,
                            quibusdam, ipsa deserunt optio.</p>
                        <div class="row">
                            <div class="col-6">
                                <div class="content">
                                    <h2 class="f-max">168</h2>
                                    <h3>User Stories</h3>
                                </div>
                            </div>
                            <div class="col-6">
                                <div class="content">
                                    <h2 class="f-max">347</h2>
                                    <h3>Events</h3>
                                </div>
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

h2,
h3 {
    font-weight: 600;
}

h3 {
    color: $a40c4ff;
}

.f-max {
    font-size: 4rem;
    color: $a40c4ff;
}

img {
    width: 70%;
    height: 70%;
    object-fit: cover;
}

p {
    color: $a847b7b;
}
</style>