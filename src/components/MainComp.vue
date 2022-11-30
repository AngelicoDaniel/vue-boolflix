<template>
    <div>
        <h2>FILM</h2>
        <MovieComp :films="films"/>

        <h2 class="p-3">SERIES</h2>
        <SeriesComp :series="series"/>
    </div>
</template>

<script>
import MovieComp from './MovieComp.vue'
import SeriesComp from './SeriesComp.vue'


    export default {
        name: 'MainComp',
        components: {
            MovieComp,
            SeriesComp
        },
        props: ['films', 'series']
    }
</script>

<style lang="scss" scoped>
div{
    color: white;
}
</style>