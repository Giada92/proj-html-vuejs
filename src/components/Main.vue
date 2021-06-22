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
  </main>
</template>

<script>
import Card from './Card.vue';

export default {
    name:"Main",
    components:{
      Card
    },
    props:{
      newTemplate: Array,
      services:Array
    }
}
</script>

<style lang="scss" scoped>

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
  height: 700px;
  padding-top: 100px;
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

</style>