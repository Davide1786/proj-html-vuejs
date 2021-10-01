<template>
  <div id="app" class="container">
    <Header />

    <MainTop />
    <MainCenter />
    <MainBottom />

    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import MainTop from './components/MainTop.vue'
import MainCenter from './components/MainCenter.vue'
import MainBottom from './components/MainBottom.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    MainTop,
    MainCenter,
    MainBottom,
    Footer
  }
}
</script>

<style lang="scss">
@import "./styles/general.scss";

  .container {
    width: 100%;
    height: 100%;
    // background: black;
  }

</style>
