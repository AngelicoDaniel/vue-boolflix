<template>
    <div>
        <CardComp
        v-for="(elem, index) in films"
        :key="index"
        :titolo="elem.name"
        :titoloOriginale="elem.original_name"
        :lingua="elem.original_language"
        :voto="elem.vote_average"
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

</style>