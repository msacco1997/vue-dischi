<template>
    <section>
        <div class="container">
            <!-- <div v-if="isLoading" class="loading"></div> -->
            <div v-cloak class="album_wrapper">
                <OneAlbum v-for="(album, index) in albums" :key="index" :OneAlbum="album" />
            </div>
        </div>
    </section>
</template>

<script>
import OneAlbum from './Album.vue'
import axios from 'axios'
export default {
    name: 'AlbumList',
    components:{
        OneAlbum,
    },
    data() {
        return {
            albums:[],
            isLoading: true,
        }
    },
    methods:{
        getAlbums: function(){
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then( res => {
                console.log(res.data.response); 
                this.albums = res.data.response; 
                
            })
            .finally( () => (this.isLoading = false))
        },
    },
    created(){ 
        this.getAlbums()
    }
}
</script>

<style lang="scss" scoped>
section{
    height: 100%;
    display: flex;
    align-items: center;
} .container{
        height: 100%;
    }
    .album_wrapper{
        height: 100%;
        display: flex;
        flex-wrap: wrap;
        gap: 15px 20px;
        padding: 1% 20%;
        .loading {
        background-color: red;
        height: 400px;
        width: 400px;
        }
    }
</style>