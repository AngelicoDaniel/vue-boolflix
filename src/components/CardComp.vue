<template>
    <div class="card">
        <div>{{cardInfo.titolo}}</div>
        <div v-if="cardInfo.titoloOriginale != cardInfo.titolo">{{cardInfo.titoloOriginale}}</div>
        <div>{{cardInfo.lingua}}</div>
        <div>Voto: {{cardInfo.voto}}</div>
        <img :src="`https://image.tmdb.org/t/p/w342${cardInfo.img}`" alt="">

    </div>
</template>

<script>
    export default {
        name: 'CardComp',
        props: {
            cardInfo: Object
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