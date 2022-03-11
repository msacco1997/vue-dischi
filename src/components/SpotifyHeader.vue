<template>
    <div class="wrapper">
        <div class="img">
            <img src="../assets/spotify_logo.png" alt="">

        </div>
    </div>
</template>

<script>
    export default {
        name: 'SpotifyHeader'
    }
</script>


<style lang="scss" scoped>
$grey: #575757;

.wrapper{
width: 100vw;
height: 100px;
background-color: $grey;
margin: 0 auto;
display: flex;
align-items: center;
    .img{
        width: 50px;
        margin-left: 20px;
        img{
            width: 70px;
        } 
    }
}
</style>
