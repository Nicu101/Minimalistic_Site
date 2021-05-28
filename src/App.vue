<template>
  <div id="app">
    <TopOfPage/>
    <AboutPart/>
    <HowToPart/>
    <Faqs/>
    <Footer/>
  </div>
</template>

<script>
import TopOfPage from './components/TopOfPage.vue'
import AboutPart from './components/AboutPart.vue'
import HowToPart from './components/HowToPart.vue'
import Faqs from './components/Faqs.vue'
import Footer from './components/Footer'

export default {
  name: 'App',
  components: {
    TopOfPage,
    AboutPart,
    HowToPart,
    Faqs,
    Footer
  }
}
</script>

<style>
#app {
  background-color: #E5E5E5;
  
}
</style>
