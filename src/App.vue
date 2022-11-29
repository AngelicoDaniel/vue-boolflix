<template>
  <div id="app">
    <HeaderComp @search="searchTitle"/>
    <MainComp :films="films"/>
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
    apiKey: '8570b8b0e80303c0c307748fd71cc35d',
    searchText: '',
    films: [],
    series: []
   }
  },
  methods: {
    searchTitle(text) {
      this.films = []
      this.searchText = text,
      console.log(this.searchText);
      
      
      axios 
           .get(`https://api.themoviedb.org/3/search/movie?api_key=${this.apiKey}&language=it_IT&query=${this.searchText}`)
           .then( (response) => {
            console.log(response.data.results);

            response.data.results.forEach(elem =>{
              let movie = {
                'titolo': elem.name,
                'titoloOriginale': elem.original_name,
                'lingua': elem.original_language,
                'voto': elem.vote_average,
                'img': elem.poster_path
              }
              this.films.push(movie)
            })
            console.log(this.films);
           })


    }
  }
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
