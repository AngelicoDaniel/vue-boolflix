<template>
    <div class="card">
        <div>{{nomeOggetto.titolo}}</div>
        <div>{{nomeOggetto.titoloOriginale}}</div>
        <div>{{nomeOggetto.lingua}}</div>
        <div>{{nomeOggetto.voto}}</div>
        <img :src="`https://image.tmdb.org/t/p/w342${nomeOggetto.img}`" alt="">

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