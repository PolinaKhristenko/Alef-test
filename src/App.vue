<template>
  <NavBar />
  <main class="main">
  <ProductItem />
  <PhotosBlock />
  </main>
  <FooterItem />
</template>

<script>

import NavBar from '@/components/NavBar'
import FooterItem from '@/components/FooterItem'
import PhotosBlock from '@/components/PhotosBlock'
import ProductItem from '@/components/ProductItem'

export default {
  name: 'App',
  components: {
    NavBar,
    ProductItem,
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
