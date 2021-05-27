<template>
  <div id="app">
    <TopOfPage/>
    <AboutPart/>
  </div>
</template>

<script>
import TopOfPage from './components/TopOfPage.vue'
import AboutPart from './components/AboutPart.vue'

export default {
  name: 'App',
  components: {
    TopOfPage,
    AboutPart,
  }
}
</script>

<style>
#app {
  background-color: #E5E5E5;
}
</style>
