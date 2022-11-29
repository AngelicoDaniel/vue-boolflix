<template>
    <div class="card">
        <div>{{nomeOggetto.titolo}}</div>
        <div v-if="nomeOggetto.titoloOriginale != nomeOggetto.titolo">{{nomeOggetto.titoloOriginale}}</div>
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
.card{
    width: calc(100% / 5);
    height: auto;
    background-color: lightgray;
    margin: 5px;
    padding: 20px;
    img{
        width: 100px;
    }
}
</style>