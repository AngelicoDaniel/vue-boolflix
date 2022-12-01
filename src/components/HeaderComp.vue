<template>
  <div class="d-flex justify-content-around align-items-center">
    <div>
       <h2 class="text-danger">BOOLFLIX</h2>
    </div>
   
    <input type="text" placeholder="cerca film e serie tv" v-model="searchText" @keyup="$emit('search', searchText)">
  </div>
</template>

<script>
export default {
  name: 'HeaderComp',
  data () {
    return {
      searchText: ''
    }
  }
}
</script>


<style scoped lang="scss">
div{
  height: 10%;
}
</style>
