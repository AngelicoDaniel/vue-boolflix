<template>
    <div class="card">
        <h5>{{cardInfo.titolo}}</h5>
        <div v-if="cardInfo.titoloOriginale != cardInfo.titolo">{{cardInfo.titoloOriginale}}</div>
        <!-- <div>{{cardInfo.lingua}}</div> -->
        <div v-if="flags.includes(cardInfo.lingua)" class="p-2">
            <img :src="require(`../assets/img/${cardInfo.lingua}.png`)" alt="" class="flags">
            <!-- <img :src=" '../assets/img/' + cardInfo.lingua + '.png' " height="100" width="100" alt=""/> -->
        </div>
        <div v-else>
            <img src="../assets/not-found.png" alt="" class="not-found">
        </div>
        <div>Voto: {{cardInfo.voto}}</div>
        <img :src="`https://image.tmdb.org/t/p/w342${cardInfo.img}`" alt="" class="poster">

    </div>
</template>

<script>
    export default {
        name: 'CardComp',
        props: {
            cardInfo: Object
        },
        data() {
            return {
                flags: ['en', 'it', 'ja', 'fr', 'de', 'es', 'ko']
            } 
        }
    }
</script>

<style lang="scss" scoped>
.card{
    width: calc(100% / 5);
    height: auto;
    background-color: #212529;
    margin: 10px;
    padding: 20px;
    align-items: center;
    border: 1px solid white;
    .poster{
        width: 200px;
    }
    .flags{
        width: 30px;
    }
    .not-found{
        width: 50px;
    }
}
</style>