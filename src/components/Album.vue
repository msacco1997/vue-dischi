<template>
    <div class="album">
        <img :src="OneAlbum.poster">
        <h5>{{OneAlbum.title}}</h5>
        <span>{{OneAlbum.author}}</span>
        <span>{{OneAlbum.year}}</span>
    </div>  
</template>

<script>
export default {
    name: 'OneAlbum',
    props:{
        OneAlbum:{
            type: Object,
            required: true,
        }
    }
}
</script>

<style lang="scss">
    .album{
        width: 18%;
        background-color: #2E3A46;
        display: flex;
        flex-direction: column;
        align-items: center;
        img{
            width: 80%;
            height: 50%;
            padding: 15px 0px 20px 0px;
        }
        h5{
            text-transform: uppercase;
            color: white;
            font-size: 18px;
            padding: 0px 10px;
        }
        span{
            color: silver;
            font-size: 14px;
            padding: 5px 0px;
        }
    }
</style>