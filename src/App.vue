<template>
  <NavBar />
  <main class="main"></main>
  <FooterItem />
</template>

<script>

import NavBar from '@/components/NavBar'
import FooterItem from '@/components/FooterItem'
export default {
  name: 'App',
  components: {
    NavBar,
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
