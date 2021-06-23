<template>
  <main>
      <!-- Sezione new Template -->
      <NewTemplate :newTemplate="newTemplate"/>
      <!-- /Sezione new Template -->

      <!-- Sezione Service -->
      <Service :services="services"/>
      <!-- /Sezione Service -->

      <!-- Sezione Our Work -->
      <Work :gallery="gallery"/>
      <!-- /Sezione Our Work -->

      <!-- Sezione Plans -->
      <section id="plans">
        <div class="container text-center">
          <h2 class="fw-bold">Our Plans</h2>
          <h5>Lorem, ipsum dolor sit amet consectetur adipisicing elit. <br>Temporibus fuga repellat, reprehenderit sit perspiciatis incidunt?</h5>
          <div class="wrapper_plans d-flex justify-content-between">
            <div v-for="plan, index in plans" :key="index" class="text-center plan_">
              <h3 class="fw-bold">{{ plan.level }}</h3>
              <div class="wrappwr_price">
                <span :class="plan.dollar" class="dollar"></span>
                <span class="price">{{ plan.price }}</span>
                <span class="cents">{{ plan.cents }}</span>
                <span class="time">{{ plan.time }}</span>
              </div>
              <div>
                <p class="fs-5 my-4">{{ plan.projects }}</p>
                <p class="fs-5 my-4">{{ plan.GB }}</p>
                <p class="fs-5 my-4">{{ plan.Users }}</p>
                <span class="fs-5 my-4 d-inline-block start">{{ plan.start }}</span>
              </div>
            </div>
          </div>
        </div>
      </section>
      <!-- /Sezione Plans -->

      <!-- Sezione News -->
      <News />
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
import Slider from './Slider.vue';
import SliderLogos from './SliderLogos.vue';
import NewTemplate from './NewTemplate.vue';
import Service from './Service.vue';
import Work from './Work.vue';
import News from './News.vue';


export default {
    name:"Main",
    components:{
      Slider,
      SliderLogos,
      NewTemplate,
      Service,
      Work,
      News
    },
    data(){
      return{
        gallery:[
          {
            url: require("../../assets/img/case-study-gallery-3-1-800x600.jpg")
          },
          {
            url: require("../../assets/img/case-study-gallery-2-800x600.jpg")
          },
          {
            url: require("../../assets/img/case-study-gallery-1-1-800x600.jpg")
          },
          {
            url: require("../../assets/img/case-study-gallery-4-1-800x600.jpg")
          },
          {
            url: require("../../assets/img/case-study-gallery-5-1-800x600.jpg")
          },
          {
            url: require("../../assets/img/case-study-gallery-6-1-800x600.jpg")
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
@import "../../assets/style/globali.scss";

/* sezione plans */
#plans {
  min-height: 900px;
  padding: 100px 0;
  background-image: url('../../assets/img/background1.jpg');
  background-size: auto;

    h2,
    h5{
    color: white;
  }
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
    font-size: 30px;
    color: $blue-light;
  }
}

.wrappwr_price{
  position: relative;
  margin: 20px 0;
  text-align: center;
  color: black;
}

.dollar{
  position: absolute;
  left: 90px;
  top: 10px;
}

.price{
  font-size: 40px;
  font-weight: 700;
  color: $blue-light;
}

.cents {
  position: absolute;
  font-weight: 700;
  top: 8px;
  color: $blue-light;
}

.time{
  font-style: italic;
  font-size: 12px;
}

.start {
   @include btn_grey;

   &:hover {
     @include btn_orange;
     color: white;
     border: 2px solid $orange;
   }
}
/* sezione plans */

/* sezione Clients say */
#clients_say{
  padding-top: 100px;
  padding-bottom: 50px;
  overflow-x: hidden;
}

/* sezione Clients say */

/* sezione consultation */

#consultation{
    height: 500px;
    position: relative;
    background-image: url('../../assets/img/CTA-seo-1.jpg');
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