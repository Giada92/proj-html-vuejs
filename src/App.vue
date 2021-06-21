<template>
  <div id="app">
    <!-- Header della pagina -->
    <Header />
    <!-- /Header della pagina -->

    <!-- Corpo della pagina -->
    <Main />
    <!-- /Corpo della pagina -->

    <!-- Footer -->
    <Footer />
    <!-- /Footer -->

  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';

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
@import "./assets/style/globali.scss";

</style>
