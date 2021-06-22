<template>
    <div class="slider_logo d-flex d-flex justify-content-around">
        <span v-for="el, index in urlLogos" :key="index">
            <img  class="d-block" :src="el.url" :alt="el.alt">
        </span>
        
    </div>
</template>

<script>
export default {
    name:"SliderLogos",
    props:{
        urlLogos: Array
    },   
}
</script>

<style lang="scss" scoped>
/* loghi */
.slider_logos {
  padding: 10px 0;

}

img {
    height: 120px;
  }
</style>

