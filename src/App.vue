<template>
  <NavBar />
  <main class="main">
  <PhotosBlock />
  </main>
  <FooterItem />
</template>

<script>

import NavBar from '@/components/NavBar'
import FooterItem from '@/components/FooterItem'
import PhotosBlock from '@/components/PhotosBlock'

export default {
  name: 'App',
  components: {
    NavBar,
    PhotosBlock,
    FooterItem
  }
}
</script>

<style>
#app {
  overflow: hidden;
  min-height: 100%;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-orient: vertical;
  -webkit-box-direction: normal;
  -ms-flex-direction: column;
  flex-direction: column;
}
</style>
