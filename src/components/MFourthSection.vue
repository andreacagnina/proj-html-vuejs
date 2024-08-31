<script>
export default {
    data() {
        return {
            infos: [
                'What We Do',
                'Degree Programme',
                'Career Achievements',
                'Personal Managment',
                'Steps To Success',
                'Knowledge Transfer',
            ],
            currentIndex: 0,
        }
    }
}
</script>

<template>
    <div class="card">
        <ul class="list-group list-group-flush">
            <li class="list-group-item" v-for="(label, index) in infos" :key="index">{{ label }}</li>

        </ul>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/Colors' as*;
</style>