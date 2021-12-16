<template>
  <header class="ps-3">
     <img src="../../assets/img/spotify-logo.png" alt="Spotify"> 
  </header>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style lang='scss' scoped>

header {
  background-color: #2E3A46;
  height: 80px;
  display: flex;
  align-items: center;
  justify-content: flex-start;
}

img {
  height: 50px;
}

</style>