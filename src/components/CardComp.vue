<template>
    <div class="card">
        <div>{{nomeOggetto.titolo}}</div>
        <div>{{nomeOggetto.titoloOriginale}}</div>
        <div>{{nomeOggetto.lingua}}</div>
        <div>{{nomeOggetto.voto}}</div>

    </div>
</template>

<script>
    export default {
        name: 'CardComp',
        props: {
            nomeOggetto: Object
        }
    }
</script>

<style lang="scss" scoped>

</style>