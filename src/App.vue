<template>
    <Nav />
</template>

<script>

import Nav from '@/components/Nav'
export default {
  name: 'App',
  components: {
    Nav
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
