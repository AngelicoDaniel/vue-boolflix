<template>
    <div class="card">
        <div>{{titolo}}</div>
        <div>{{lingua}}</div>
        <div>{{voto}}</div>

    </div>
</template>

<script>
    export default {
        name: 'CardComp',
        props: {
            titolo: String,
            titoloOriginale: String,
            lingua: String,
            voto: Number
        }
    }
</script>

<style lang="scss" scoped>

</style>