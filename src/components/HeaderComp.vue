<template>
  <div>
    <h2 class="text-danger">BOOLFLIX</h2>
    <input type="text" v-model="searchText" @keyup="$emit('search', searchText)">
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
