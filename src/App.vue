<template>
  <div id="app" class="container">
    <Header />

    <Main msg=""/>

    <Footer msg=""/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
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
