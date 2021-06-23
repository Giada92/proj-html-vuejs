<template>
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
</template>

<script>
import Card from './Card.vue';

export default {
    name:"Service",
    props:{
        services: Array
    },
    components:{
        Card
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/globali.scss";

/* Sezione Service */
#service {
  padding: 100px 0;
  background-image: url('../../assets/img/pattern_background.png');
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