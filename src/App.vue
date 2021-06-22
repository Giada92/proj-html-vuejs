<template>
  <div id="app">
    <!-- Header della pagina -->
    <Header :links="links"/>
    <!-- /Header della pagina -->

    <!-- Corpo della pagina -->
    <Main :newTemplate="newTemplate"
          :services="services"
          :clients="clients"
          :urlLogos="urlLogos"
          :plans="plans"/>
    <!-- /Corpo della pagina -->

    <!-- Footer -->
    <Footer :links="links"
            :info="info"/>
    <!-- /Footer -->

    <!-- Pulsante per tornare in cima alla pagina - Fixed -->
    <div id="arrow">
        <a class="btn" href="#"><i class="fas fa-chevron-up"></i></a>
    </div>        
    <!-- Pulsante per tornare in cima alla pagina - Fixed -->

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
          job: "Architect"
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
      ],
      plans: [
        {
          level:"Standard",
          dollar:"fas fa-dollar-sign",
          price: "19",
          cents: "99",
          time: "monthly",
          projects:"5 Projects",
          GB: "5 GB Storage",
          Users:"Unlimited Users",
          start:"Start Today"
        },
        {
          level:"Premium",
          dollar:"fas fa-dollar-sign",
          price: "29",
          cents: "99",
          time: "monthly",
          projects:"10 Projects",
          GB: "15 GB Storage",
          Users:"Unlimited Users",
          start:"Start Today"
        },
        {
          level:"Professional",
          dollar:"fas fa-dollar-sign",
          price: "39",
          cents: "99",
          time: "monthly",
          projects:"15 Projects",
          GB: "30 GB Storage",
          Users:"Unlimited Users",
          start:"Start Today"
        },
        {
          level:"Extrame",
          dollar:"fas fa-dollar-sign",
          price: "59",
          cents: "99",
          time: "monthly",
          projects:"Unlimited Projects",
          GB: "Unlimited Storage",
          Users:"Unlimited Users",
          start:"Start Today"
        }
      ]
    }
  }
}
</script>

<style lang="scss">
@import "./assets/style/globali.scss";

/* Pulsante Help */
#arrow {
    position: fixed;
    width: 40px;
    bottom: 0%;
    right: 5%;
    background-color: rgba(0,0,0,0.8);
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;

    
    i{
       color: white;
    }
}


</style>
