<template>
  <div id="app">
    <div class="container">
      <Navbar />
      <Content />
    </div>
    
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Content from './components/Content.vue'
export default {
  name: 'App',
  components: {
    Navbar,
    Content
  }
}
</script>

<style scoped>
  .container {
    padding: 20px;
    margin: 0 auto;
    max-width: 1100px;
    background-color: #fff;
    z-index: 99;
    position: fixed;
    left: 0;
    top: 0;
    right: 0;
  }
</style>
