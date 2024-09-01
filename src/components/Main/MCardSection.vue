<script>
import { matterCards } from "../../data/CardsSection";
export default {
    data() {
        return {
            matterCards,
        }
    }

}
</script>

<template>
    <div class="container my-5">
        <div class="row">
            <div class="col-6 col-md-4 g-2 col-lg-2" v-for="(card, index) in matterCards" :key="`card-${index}`">
                <a href="#">
                    <div class="content matter-card p-5 p-md-2">
                        <img :src="card.url" alt="img matter">
                        <h4>{{ card.title }}</h4>
                    </div>
                </a>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/Colors' as*;

a {
    color: $a000000;
}

.matter-card {
    border: 1px solid $f2f2f2;
    background-color: $f2f8fc;
    text-align: center;
    cursor: pointer;

    &:hover {
        border: 1px solid $a40c4ff;
    }

    h4 {
        font-weight: 600;
        margin-top: 2rem;
    }

}
</style>