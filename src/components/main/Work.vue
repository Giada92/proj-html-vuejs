<template>
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
</template>

<script>
export default {
    name:"Work",
    props:{
        gallery: Array
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/globali.scss";

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
</style>