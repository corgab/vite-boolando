<script>
import HeroSection from './components/HeroSection.vue'
import ProductSection from './components/ProductSection.vue'
import FooterSection from './components/FooterSection.vue'
import { store } from './store.js'
import axios from 'axios'

export default {
  components: {
    HeroSection,
    ProductSection,
    FooterSection,
    
  },
  data() {
    return {
      store,
    }
  },
  mounted() {
    axios.get('http://localhost:3000/products')
    .then((res) => {
      // console.log(res)
      // console.log(res.data)
      this.store.data = res.data
    })
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