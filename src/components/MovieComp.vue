<template>
    <div>
        <CardComp
        v-for="(elem, index) in films"
        :key="index"
        :nomeOggetto="elem"
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