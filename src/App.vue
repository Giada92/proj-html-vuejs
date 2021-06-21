<template>
  <div id="app">
    <!-- Header della pagina -->
    <Header :links="links"/>
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
  },
  data(){
    return{
      links:[
        {
          text: "Home",
          link: "#home",
          selected: false
        },
        {
          text: "Who We Are",
          link: "#who we are",
          selected: true
        },
        {
          text: "What We Do",
          link: "#what we do",
          selected: false
        },
        {
          text: "Where We Work",
          link: "#where we work",
          selected: false
        },
        {
          text: "Careers",
          text2: "Apply",
          link: "#careers",
          selected: false
        },
        {
          text: "News",
          link: "#news",
          selected: false
        },
        {
          text: "Get In Touch Now",
          link: "#get in touch now",
          selected: false
        }
      ]
    }
  }
}
</script>

<style lang="scss">
@import "./assets/style/globali.scss";

</style>
