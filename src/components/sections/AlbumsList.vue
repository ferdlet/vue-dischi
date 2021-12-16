<template>
  <section id="albums-list" class="container">

        <div class="album_container" v-for="(album, index) in albums" :key="index">
          <Album :info="album"/>
        </div>

  </section>
</template>

<script>
import axios from 'axios';
import Album from '../commons/Album.vue'

export default {
    name: 'AlbumsList',
    components: {
      Album
    },
    data() {
      return {
        albums: null
      }
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            // handle success
            this.albums = response.data.response;
            console.log(response.data.response);
        })
        .catch(function (error) {
            // handle error
            console.log(error);
        });
    }
}
</script>

<style lang='scss' scoped>
  #albums-list {
    padding: 50px 0;
    // margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    .album_container {
      width: calc(100% - 40px);
      margin: 20px;
      @media screen and (min-width: 576px) {
        width: calc(100% / 2 - 40px);
      }
      @media screen and (min-width: 768px) {
        width: calc(100% / 3 - 40px);
      }
      @media screen and (min-width: 992px) {
        width: calc(100% / 5 - 40px);
      }
    }
  }
</style>