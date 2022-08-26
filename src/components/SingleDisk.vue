<template>
    <div class="disk-card">
        <img :src="disk.poster" alt="">
        <h3>{{disk.title}}</h3>
        <h4>{{disk.author}}</h4>
        <h5>{{disk.year}}</h5>
    </div>
</template>

<script>
export default {
    name: 'SingleDisk',
    props: {
        disk: Object
    },
    mounted(){
        console.log(typeof this.disk);
    }
}
</script>

<style scoped lang="scss">
    .disk-card {
        width: calc((100% / 5) - 30px);
        padding-top: 50px;
        margin: 15px 15px;
        text-align: center;
        background-color: #2E3A46;
        cursor: pointer;
        &:hover {
            outline: 1px solid #fff;
        }
        img {
            width: 150px;
            height: 150px;
        }
        h3 {
            color: white;
            text-transform: uppercase;
            font-size: 16px;
            padding: 10px 0;
        }
        h4, h5 {
            color: grey;
            padding: 1px 0;
        }
    }
</style>