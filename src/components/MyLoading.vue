<template>
  <div class='loading'>
    <h2>Attendere.. Caricamento in corso...</h2>
  </div>
</template>

<script>
export default {
    name: 'MyLoading'
}
</script>

<style scoped lang="scss">
    .loading {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: grey;
        h2 {
            font-size: 50px;
            color: #000;
        }
    }
</style>