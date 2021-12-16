<template>
  <div class="album text-center p-3">
        <img :src="info.poster" :alt="info.title">
        <h4 class="my-4">{{info.title}}</h4>
        <p>{{info.author}}</p>
        <p>{{info.year}}</p>
  </div>
</template>

<script>
export default {
    name: 'Album',
    props: {
        info: Object
    }
}
</script>

<style lang='scss' scoped>
    .album {
        height: 100%;
        background-color: #2E3A46;
        h4 {
            color: white;
            font-size: 18px;
            font-weight: bold;
            text-transform: uppercase;
        }
        img {
            width: 100%;
        }
        p {
            margin: 0;
            font-size: 16px;
            color: #777;
        }
    }
    
</style>