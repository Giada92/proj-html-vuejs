<template>
  <main>
      <!-- Sezione new Template -->
      <section id="new_template">
        <!-- Contenitore -->
        <div class="container">
          <h2 class="text-center fw-bold">Meet The New Agency SEO Template<br> From The Avada Team</h2>
          <p class="text-center">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sequi, qui.</p>

          <!-- Contenitore flex per le 3 card -->
          <div class="d-flex my-5">
            <div v-for="el,index in newTemplate" :key="index"
                class="text-center py-5 px-4 wrapper_card">
                <Card :icon="el.icon" :title="el.title" :text="el.text"/>
            </div>
          </div>
          <!-- /Contenitore flex per le 3 card -->

          <img class="img_new_template" src="../assets/img/agency-seo-desk-front-1200x570.jpg" alt="Immagine Scrivania Ufficio">
        </div>
        <!-- /Contenitore -->
      </section>
      <!-- /Sezione new Template -->

      <!-- Sezione Service -->
      <section id="service">
        <div class="container">
          <h2 class="text-center fw-bold">See Our Top Notch Services</h2>
          <p class="text-center">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sequi, qui.</p>
          <div class="d-flex my-5">
            <div v-for="service,index in services" :key="index"
                class="text-center py-5 px-4 wrapper_card_service">
                <Card :icon="service.icon" :title="service.title" :text="service.text" :link="service.link"/>
            </div>
          </div>
        </div>
      </section>
      <!-- /Sezione Service -->

      <!-- Sezione Our Work -->
      <section id="work">
        <div class="container">
            <h2 class="text-center fw-bold">Our Work</h2>
            <p class="text-center">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sequi, qui.</p>
            <div class="d-flex flex-wrap justify-content-center">
              <!-- Contenitore gallery che cicla le foto-->
              <div class="wrapper_gallery" v-for="el, index in gallery" :key="index">
                <div class="gallery_img">
                  <img :src="el.url" alt="">
                  <div class="d-flex justify-content-center align-items-center layover">
                    <i class="fas fa-link"></i>
                  </div>
                </div>
              </div>
              <!-- /Contenitore gallery che cicla le foto-->
            </div>
            <div class="text-center mt-5">
              <span class="btn_orange">View our work </span>
            </div>
        </div>
      </section>
      <!-- /Sezione Our Work -->

      <!-- Sezione Clients say -->
      <section id="clients_say" class="container text-center">
        <h2 class="fw-bold">What Our Clients Say</h2>
        <Slider :clients="clients"/>
        <hr class="my-5">
        <SliderLogos :urlLogos="urlLogos"/>
      </section>
      <!-- /Sezione Clients say -->

  </main>
</template>

<script>
import Card from './Card.vue';
import Slider from './Slider.vue';
import SliderLogos from './SliderLogos.vue';



export default {
    name:"Main",
    components:{
      Card,
      Slider,
      SliderLogos
    },
    data(){
      return{
        gallery:[
          {
            url: require("../assets/img/case-study-gallery-3-1-800x600.jpg")
          },
          {
            url: require("../assets/img/case-study-gallery-2-800x600.jpg")
          },
          {
            url: require("../assets/img/case-study-gallery-1-1-800x600.jpg")
          },
          {
            url: require("../assets/img/case-study-gallery-4-1-800x600.jpg")
          },
          {
            url: require("../assets/img/case-study-gallery-5-1-800x600.jpg")
          },
          {
            url: require("../assets/img/case-study-gallery-6-1-800x600.jpg")
          }
        ]
      }
    },
    props:{
      newTemplate: Array,
      services:Array,
      clients: Array,
      urlLogos: Array
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/globali.scss";

/* Sezione new Template */
#new_template {
    padding-top: 100px;
    background-color: #F7F8FA;
}

.wrapper_card {
  width: calc(100% / 3 - 20px);
  margin: 0 10px;
  background-color: white;
}

.img_new_template {
  object-position: 50px;
}
/* Sezione new Template */

/* Sezione Service */
#service {
  padding: 100px 0;
  background-image: url('../assets/img/pattern_background.png');
  background-size: contain;
  background-color: #051642;
  color: white;
}

.wrapper_card_service {
  width: calc(100% / 4 - 20px);
  margin: 0 10px;
  background-color: #071B50;
}
/* Sezione Service */

/* Sezione Work */

#work {
  width: 100%;
  padding: 100px 0;
}

.wrapper_gallery {
  width: calc(100% / 3 );
  margin: 10px 0;
}

.gallery_img:hover > .layover {
    visibility: visible;
}

.gallery_img {
    position: relative;
}

.gallery_img{
    img {
    display: block;
    max-width: 95%;
    object-fit: cover;
  }
}

.layover {
    width: 95%;
    height: 100%;
    position: absolute;
    top:0;
    left: 0;
    background-color: rgba(#0369d7, 0.5);
    color: white;
    cursor: pointer;
    visibility: hidden;

    & > i {
    font-size: 40px;
}
}

.btn_orange {
    @include btn_orange;
    padding: 15px 25px;
    margin-right: 15px;
    color: white;

    &:hover{
        background-color: $orange-light;
    }
}

/* Sezione Work */

/* sezione Clients say */
#clients_say{
  padding: 100px 0;
}

/* sezione Clients say */

</style>