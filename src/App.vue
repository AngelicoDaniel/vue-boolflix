<template>
  <div id="app">
    <HeaderComp @search="searchTitle"/>
    <MainComp/>
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'
import MainComp from './components/MainComp.vue'
import axios from 'axios'


export default {
  name: 'App',
  components: {
    HeaderComp,
    MainComp
  },
  data() {
   return {
    APIKey: '8570b8b0e80303c0c307748fd71cc35d',
    searchText: '',
    films: [],
    series: []
   }
  },
  methods: {
    searchTitle(text) {
      this.searchText = text,
      console.log(this.searchText);
      
      
      axios.get( `https://api.themoviedb.org/3/movie/550?api_key=${this.APIKey}&query=${this.searchText}&language=it-IT` )
           .then( (response) => {
            console.log(response.data.response);
           })


    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
