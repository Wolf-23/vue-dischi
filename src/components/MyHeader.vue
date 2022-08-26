<template>
    <header>
        <img src="../assets/logo-small.png" alt="Logo Spotify">
    </header>
</template>

<script>
export default {
    name: 'MyHeader'
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
    img {
        height: 80%;
        padding-left: 15px;
    }
   }
</style>