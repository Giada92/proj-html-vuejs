<template>
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

          <img class="img_new_template" src="../../assets/img/agency-seo-desk-front-1200x570.jpg" alt="Immagine Scrivania Ufficio">
        </div>
        <!-- /Contenitore -->
      </section>
</template>

<script>
import Card from './Card.vue';

export default {
    name:"NewTemplate",
    props:{
        newTemplate:Array
    },
    components:{
        Card
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/globali.scss";

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

</style>