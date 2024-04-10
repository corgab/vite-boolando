<script>
// primo passaggio imporare il componente
import HeroSection from './components/HeroSection.vue'
import ProductSection from './components/ProductSection.vue'

export default {
  // secondo passaggio registrare il componente
  components: {
    HeroSection,
    ProductSection
    
  },
  data() {
    return {
      message: 'Hello world!'
    }
  }
}
</script>

<template>
  <!-- Utilizzare il componente nel template -->
  <HeroSection />
  <ProductSection />
</template>

<!-- qui non ci deve essere l'attributo scoped -->
<style lang="scss">
// ultimo passaggio importaimo il file general con gli stili globali
@use './style/general';

</style>