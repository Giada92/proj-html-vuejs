<template>
  <div id="app">
    <!-- Header della pagina -->
    <Header :links="links"/>
    <!-- /Header della pagina -->

    <!-- Corpo della pagina -->
    <Main :newTemplate="newTemplate"
          :services="services"
          :clients="clients"
          :urlLogos="urlLogos"/>
    <!-- /Corpo della pagina -->

    <!-- Footer -->
    <Footer :links="links"
            :info="info"/>
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
      ],
      info:[
        {
          name: "Copyright 2012-2020"
        },
        {
          name: "Avada Theme by",
          by:"ThemeFusion"
        },
        {
          name: "All Rights Reserved"
        },
        {
          name: "Powered by",
          by:"WordPress"
        }
      ],
      newTemplate:[
        {
          icon: "fas fa-road",
          title: "Establish Goals",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid nesciunt ipsam, adipisci quasi ea voluptatibus."
        },
        {
          icon: "fas fa-video",
          title: "Work With a Team",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid nesciunt ipsam, adipisci quasi ea voluptatibus."
        },
        {
          icon: "fas fa-tint",
          title: "Get Results",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid nesciunt ipsam, adipisci quasi ea voluptatibus."
        }
      ],
      services:[
        {
          icon: "fab fa-google",
          title: "Google Seo",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid nesciunt ipsam, adipisci quasi ea voluptatibus.",
          link: "Read More"
        },
        {
          icon: "fas fa-cog",
          title: "Brand Strategy",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid nesciunt ipsam, adipisci quasi ea voluptatibus.",
          link: "Read More"
        },
        {
          icon: "fas fa-building",
          title: "Local SEO",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid nesciunt ipsam, adipisci quasi ea voluptatibus.",
          link: "Read More"
        },
        {
          icon: "fas fa-chart-bar",
          title: "SEO Analysis",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid nesciunt ipsam, adipisci quasi ea voluptatibus.",
          link: "Read More"
        },
      ],
      clients:[
        {
          url:require("./assets/img/testimonials-2.jpg"),
          text: "Ability proceeds from a fusion of skills, knowledge, understanding and imagination, consolidated by expierience.",
          testimonials: "Luis Desalvo",
          job: "Creo Tech"
        },
        {
          url:require("./assets/img/testimonials-1.jpg"),
          text: "Beauty is when you can appreciate yourself. When you love yourself, that's when you're most beautiful",
          testimonials: "Sheila McCourtney",
          job: "Architech"
        }
      ],
      urlLogos:[
        {
          url:require("./assets/img/clients_partner_1-200x202.png"),
          alt: "Logo Avada"
        },
        {
          url:require("./assets/img/clients_partner_2-200x202.png"),
          alt: "Logo Avada LAW"
        },
        {
          url:require("./assets/img/clients_partner_3-200x202.png"),
          alt: "Logo Avada VET"
        },
        {
          url:require("./assets/img/clients_partner_4-200x202.png"),
          alt: "Logo Avada HEALTH"
        },
        {
          url:require("./assets/img/clients_partner_5-200x202.png"),
          alt: "Logo Avada"
        },
        {
          url:require("./assets/img/clients_partner_6-200x202.png"),
          alt: "Logo Avada"
        },
      ]
    }
  }
}
</script>

<style lang="scss">
@import "./assets/style/globali.scss";

</style>
