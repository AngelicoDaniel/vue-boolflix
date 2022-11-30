<template>
    <div class="row gx-2">
        <CardComp
        v-for="(elem, index) in series"
        :key="index"
        :cardInfo="elem"
        />
    </div>
</template>

<script>
import CardComp from './CardComp.vue'

    export default {
        name: 'SeriesComp',
        components: {
            CardComp
        },
        props: ['series']

    }
</script>

<style lang="scss" scoped>

</style>