<template>
    <div>
        <CardComp
        v-for="(elem, index) in films"
        :key="index"
        :cardInfo="elem"
        />
    </div>
</template>

<script>
import CardComp from './CardComp.vue'

    export default {
        name: 'MovieComp',
        components: {
            CardComp
        },
        props: ['films']
    }
</script>

<style lang="scss" scoped>
div{
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-around;
    width: 80%;
    margin: auto;
}
</style>