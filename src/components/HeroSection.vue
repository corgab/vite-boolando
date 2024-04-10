<script>
export default {
  data() {
    return {
      //   src: 'vite.svg'
    }
  }
}
</script>

<template>
  <section class="page-header">
    <nav class="container">
      <div class="row">
        <ul class="flex">
          <li>Donna</li>
          <li>Uomo</li>
          <li>Bambini</li>
        </ul>

        <a class="logo" href="#">
          <img src="/img/boolean-logo.png" alt="" />
        </a>

        <ul class="flex">
          <li>&hearts;</li>
          <li>&hearts;</li>
          <li>&hearts;</li>
        </ul>
      </div>
    </nav>
  </section>
</template>

<style lang="scss" scoped>
.page-header {
  background-color: #fe6900;
  color: white;
  padding: 16px 0;
  box-shadow: 0px 0px 20px 2px rgba(0, 0, 0.1);
}

.row {
  justify-content: space-between;
  align-items: center;

  ul {
    gap: 20px;
  }
}

.logo img {
  height: 32px;
}
</style>