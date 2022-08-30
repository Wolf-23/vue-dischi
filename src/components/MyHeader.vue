<template>
    <header>
        <img src="../assets/logo-small.png" alt="Logo Spotify">
        <div class="ricerca">
            <select @change="$emit('changedGenre', selectedGenre)" v-model="selectedGenre">
                <option value="">Seleziona un genere:</option>
                <option v-for="(genre, index) in genresList" :key="index" :value="genre">{{genre}}</option>
            </select>
        </div>
    </header>
</template>

<script>
export default {
    name: 'MyHeader',
    props: {
        genresList: Array
    },
    data() {
        return {
            selectedGenre: ''
        }
    }
}
</script>

<style lang="scss">
  @import '../assets/styles/general.scss';
   header {
    width: 100%;
    height: 80px;
    background-color: #2E3A46;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 15px;
    img {
        height: 80%;
    }
    .ricerca {
       color: #fff;
       padding: 0 10px;
    }
    select {
        padding: 5px;
    }
   }
</style>