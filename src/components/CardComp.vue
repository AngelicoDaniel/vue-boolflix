<template>
    <div class="col-2">
        <div class="card">
            <div class="hover">
                <h5>{{cardInfo.titolo}}</h5>
                <div v-if="cardInfo.titoloOriginale != cardInfo.titolo">{{cardInfo.titoloOriginale}}</div>
                <div v-if="flags.includes(cardInfo.lingua)" class="p-2">
                    <img :src="require(`../assets/img/${cardInfo.lingua}.png`)" alt="" class="flags">
                </div>
                <div v-else>
                    <img src="../assets/missing-flag.png" alt="" class="not-found">
                </div>
                <div class="overview">
                    <span v-if="cardInfo.overview == ''"></span>
                    <span v-else>Overview: {{cardInfo.overview}}</span>
                </div>
                <div>Voto: {{Math.ceil(cardInfo.voto/2)}}</div>
            </div>
            <img v-if="(cardInfo.img == null)" class="not-found" src="../assets/not-found.png" alt="">
            <img v-else :src="`https://image.tmdb.org/t/p/w342${cardInfo.img}`" alt="" class="poster">
        </div>  
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
    height: 100%;
    align-items: center;
    border: 1px solid white;
    justify-content: center;
    background-color: #212529;
    position: relative;
    min-height: 380px;
    .poster{
        width: 100%;
        display: block;
    }
    .flags{
        width: 30px;
    }
    .not-found{
        width: 50px;
    }
    .hover{
        display: none;
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        overflow: auto;
        padding: 15px;
        min-height: 0;
    }
    .overview{
        font-size: 12px;
    }
}
.card:hover{
    .poster{
        display: none;
    }
    .hover{
        display: block;
    }
}

</style>