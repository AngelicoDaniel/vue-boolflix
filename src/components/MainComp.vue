<template>
    <div>
        <MovieComp :films="films"/>
    </div>
</template>

<script>
import MovieComp from './MovieComp.vue'

    export default {
        name: 'MainComp',
        components: {
            MovieComp
        },
        props: ['films']
    }
</script>

<style lang="scss" scoped>

</style>