<template>
    <div>
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
div{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    width: 80%;
    margin: auto;
    align-items: stretch;
}
</style>