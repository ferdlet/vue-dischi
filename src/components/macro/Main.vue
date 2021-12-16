<template>
  <main>
    <AlbumsList/>
  </main>
</template>

<script>
import AlbumsList from '../sections/AlbumsList.vue'

export default {
    name: 'Main',
    components: {
      AlbumsList,
    },
}
</script>

<style>
  main {
      background-color: #1E2D3B;
      min-height: calc(100vh - 80px);
  }
</style>
