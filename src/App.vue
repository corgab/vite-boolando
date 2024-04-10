<script>
import HeroSection from './components/HeroSection.vue'
import ProductSection from './components/ProductSection.vue'
import FooterSection from './components/FooterSection.vue'

export default {
  components: {
    HeroSection,
    ProductSection,
    FooterSection
    
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