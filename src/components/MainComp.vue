<template>
    <div>
        <MovieComp :films="films"/>
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

</style>