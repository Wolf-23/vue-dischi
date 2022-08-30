<template>
  <div id="app">
   <MyHeader @changedGenre="startSearch" :genresList="genresList"/>
   <MyMain @genresReady="getGenresList" :genreToSearch="genreToSearch"/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'


export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain
  },
  data() {
    return {
      genresList : [],
      genreToSearch: ''
    }
  },
  methods: {
    getGenresList(allGenres) {
      this.genresList = allGenres;
    },
    startSearch(genreToSearch) {
      this.genreToSearch = genreToSearch;
    }
  }
}
</script>

<style lang="scss">

</style>
