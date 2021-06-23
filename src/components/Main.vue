<template>
  <main>
      <!-- Sezione new Template -->
      <section id="new_template">
        <!-- Contenitore -->
        <div class="container">
          <h2 class="text-center fw-bold">Meet The New Agency SEO Template<br> From The Avada Team</h2>
          <h5 class="text-center my-4">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sequi, qui.</h5>

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
          <h5 class="text-center my-4">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sequi, qui.</h5>
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
            <h5 class="text-center my-4">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sequi, qui.</h5>
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

      <!-- Sezione Plans -->
      <section id="plans">
        <div class="container text-center">
          <h2 class="fw-bold">Our Plans</h2>
          <h5>Lorem, ipsum dolor sit amet consectetur adipisicing elit. <br>Temporibus fuga repellat, reprehenderit sit perspiciatis incidunt?</h5>
          <div class="wrapper_plans d-flex justify-content-between">
            <div v-for="plan, index in plans" :key="index" class="text-center plan_">
              <h3 class="fw-bold">{{ plan.level }}</h3>
              <div class="price">
                <!-- span -->
              </div>
            </div>
            <!-- DA FINIREEEEEEEEEEEEE -->
          </div>
        </div>
      </section>
      <!-- /Sezione Plans -->

      <!-- Sezione News -->
      <section id="news">
        <div class="container">
          <h2 class="text-center fw-bold">Our News</h2>
          <h5 class="text-center my-4">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sequi, qui.</h5>
          <div class="d-flex flex-wrap justify-content-center">
              <div class="wrapper_gallery">
                <div class="gallery_img">
                  <img src="../assets/img/related-service-2-700x441.jpg" alt="">
                </div>
                  <div class="text-center">
                    <h4 class="mt-2 fw-bold">Why You Need A SEO Agency Now</h4>
                    <span>November 1st, 2017</span>
                    <p class="my-4">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatem ipsam enim sapiente porro aliquam veniam?</p>
                  </div>
              </div>
              <div class="wrapper_gallery">
                <div class="gallery_img">
                  <img src="../assets/img/related-service-4-700x441.jpg" alt="">
                </div>
                  <div class="text-center">
                    <h4 class="mt-2 fw-bold">SEO Tips For Yours Startup</h4>
                    <span>November 1st, 2017</span>
                    <p class="my-4">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatem ipsam enim sapiente porro aliquam veniam?</p>
                  </div>
              </div>
              <div class="wrapper_gallery">
                <div class="gallery_img">
                  <img src="../assets/img/blog-post-6-700x441.jpg" alt="">
                </div>
                  <div class="text-center">
                    <h4 class="mt-2 fw-bold">Image Optimization For Your Site</h4>
                    <span>November 1st, 2017</span>
                    <p class="my-4">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatem ipsam enim sapiente porro aliquam veniam?</p>
                  </div>
              </div>
          </div>
          <div class="text-center mt-5">
            <span class="btn_orange">Go to the news</span>
          </div>
        </div>
      </section>
      <!-- /Sezione News -->

      <!-- Sezione Clients say -->
      <section id="clients_say" class="container text-center">
        <h2 class="fw-bold">What Our Clients Say</h2>
        <Slider :clients="clients"/>
        <hr class="my-5">
        <SliderLogos :urlLogos="urlLogos"/>
      </section>
      <!-- /Sezione Clients say -->

      <!-- Sezione Consultation -->
      <section id="consultation" class="d-flex">
          <div class="wrapper_text text-center">
              <h2 class="fw-bold">Start Your Free Consultation</h2>
              <h5 class="my-4">Lorem ipsum dolor sit amet consectetur, <br>adipisicing elit. Nemo vel beatae, molestias maxime maiores ex.</h5>
              <span>Contact us now</span>
          </div>
      </section>
      <!-- /Sezione Consultation -->
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
      urlLogos: Array,
      plans: Array
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

/* sezione news */
#news{
  padding: 100px 0;
  background-color: #F7F8FA;

  .gallery_img{
    overflow: hidden;
    max-width: 95%;
    max-height: 100%;
  }

  .gallery_img img {
     transition: all 1s ease-in-out;
  }

  .gallery_img:hover img{
    cursor: pointer;
    transform: scale(1.1);
  }
}

h4{
  color: $orange;
}

p{
  font-size: 17px;
}
/* sezione news */


/* sezione Clients say */
#clients_say{
  padding-top: 100px;
  padding-bottom: 50px;
  overflow-x: hidden;
}

/* sezione Clients say */

/* sezione plans */
#plans {
  min-height: 900px;
  padding: 100px 0;
  background-image: url('../assets/img/background1.jpg');
  background-size: auto;
  color: white;
}

.wrapper_plans {
  min-height: 500px;
}

.plan_ {
  width: calc(100% / 4 - 10px);
  margin: 40px 5px;
  padding: 15px;
  background-color: white;
  cursor: pointer;

  h3 {
    color: $blue-light;
  }
}

.price{
  position: relative;

}
/* sezione plans */

/* sezione consultation */

#consultation{
    height: 500px;
    position: relative;
    background-image: url('../assets/img/CTA-seo-1.jpg');
    background-position-y: -50px;

    &::after{
      content: "";
      position: absolute;
      top:0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.6);
    }

    .wrapper_text{
      margin: auto;
      color: white;
      z-index: 3;

      span {
        @include btn_orange;
        padding: 15px 25px;
        display: inline-block;

        &:hover{
        background-color: $orange-light;
    }
      }
    }
}

/* sezione consultation */


</style>