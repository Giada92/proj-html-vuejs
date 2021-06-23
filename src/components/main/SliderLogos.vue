<template>
    <flickity ref="flickity" :options="flickityOptions">
        <div class="carousel-cell">
            <img src="../../assets/img/clients_partner_1-200x202.png" alt="Logo Avada">
        </div>
        <div class="carousel-cell">
            <img src="../../assets/img/clients_partner_2-200x202.png" alt="Logo Avada LAW">
        </div>
        <div class="carousel-cell">
            <img src="../../assets/img/clients_partner_3-200x202.png" alt="Logo Avada VET">
        </div>
        <div class="carousel-cell">
            <img src="../../assets/img/clients_partner_4-200x202.png" alt="Logo Avada HEALTH">
        </div>
        <div class="carousel-cell">
            <img src="../../assets/img/clients_partner_5-200x202.png" alt="Logo Avada">
        </div>
        <div class="carousel-cell">
            <img src="../../assets/img/clients_partner_6-200x202.png" alt="Logo Avada">
        </div>
    </flickity>
</template>

<script>
import Flickity from 'vue-flickity';

export default {
    name:"SliderLogos",
    components:{
        Flickity
    },
    data(){
        return{
                flickityOptions: {
                initialIndex: 1,
                prevNextButtons: false,
                pageDots: false,
                wrapAround: true,
                autoPlay: 3000,
            }
        }
    }
};
</script>

<style lang="scss" scoped>

.slider_logos {
  padding: 10px 0;
}

img {
    height: 120px;
    margin: 0 200px;
  }


</style>