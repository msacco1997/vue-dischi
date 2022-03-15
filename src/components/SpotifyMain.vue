<template>
    <main>
        <AlbumList />
    </main>
</template>

<script>
import AlbumList from './AlbumList.vue'
export default {
    name: 'SpotiMain',
    components:{
        AlbumList,
    }
}
</script>

<style lang="scss">
    main{
        height: 90vh;
        background-color: #1E2D3B;
        display: flex;
        align-items: center;
        justify-content: space-around;
    }
</style>