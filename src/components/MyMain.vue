<template>
   <main>
        <div class="disk-container">
            <MyLoading v-if="load"/>
            <SingleDisk  v-for="(disk, index) in diskList" :key="index" :disk="disk" />
        </div>
   </main>
</template>

<script>
import axios from "axios"
import SingleDisk from './SingleDisk.vue'
import MyLoading from './/MyLoading.vue'

export default {
    name: 'MyMain',
    components: {
        SingleDisk,
        MyLoading
    },

    data() {
        return {
            diskList: [],
            load: true
        }
    },
    created() {
        this.getDisk();
    },
    methods: {
        getDisk() {
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then(response => {
                this.diskList = response.data.response;
                this.load = false
            })
        }
    }
}


</script>

<style scoped lang="scss">
  @import '../assets/styles/general.scss';
   main {
    width: 100%;
    height: calc(100vh - 80px);
    background-color:#1E2D3B;
    position: relative;
    .disk-container {
        display: flex;
        flex-wrap: wrap;
        width: 1170px;
        margin: 0 auto;
        padding-top: 50px;
    }
   }
</style>