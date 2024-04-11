<script>
import HeroSection from './components/HeroSection.vue'
import ProductSection from './components/ProductSection.vue'
import FooterSection from './components/FooterSection.vue'
import HelloWorld from './components/HelloWorld.vue'
import DataBase from './assets/db.json'

export default {
  components: {
    HeroSection,
    ProductSection,
    FooterSection,
    HelloWorld
    
  },
  data() {
    return {
      message: 'Hello world!'
    }
  }
}

</script>

<template>
  <HeroSection />
  <ProductSection />
  <FooterSection/>
</template>

<style lang="scss">
@use './style/general';

</style>