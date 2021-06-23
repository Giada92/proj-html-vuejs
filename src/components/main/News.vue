<template>
  <section id="news">
        <div class="container">
          <h2 class="text-center fw-bold">Our News</h2>
          <h5 class="text-center my-4">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sequi, qui.</h5>
          <div class="d-flex flex-wrap justify-content-center">
              <div class="wrapper_gallery">
                <div class="gallery_img">
                  <img src="../../assets/img/related-service-2-700x441.jpg" alt="">
                </div>
                  <div class="text-center">
                    <h4 class="mt-2 fw-bold">Why You Need A SEO Agency Now</h4>
                    <span>November 1st, 2017</span>
                    <p class="my-4">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatem ipsam enim sapiente porro aliquam veniam?</p>
                  </div>
              </div>
              <div class="wrapper_gallery">
                <div class="gallery_img">
                  <img src="../../assets/img/related-service-4-700x441.jpg" alt="">
                </div>
                  <div class="text-center">
                    <h4 class="mt-2 fw-bold">SEO Tips For Yours Startup</h4>
                    <span>November 1st, 2017</span>
                    <p class="my-4">Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatem ipsam enim sapiente porro aliquam veniam?</p>
                  </div>
              </div>
              <div class="wrapper_gallery">
                <div class="gallery_img">
                  <img src="../../assets/img/blog-post-6-700x441.jpg" alt="">
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
</template>

<script>
export default {
    name:"News"
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/globali.scss";

.wrapper_gallery {
  width: calc(100% / 3 );
  margin: 10px 0;
}

.gallery_img{
    img {
    display: block;
    max-width: 95%;
    object-fit: cover;
  }
}

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

.btn_orange {
    @include btn_orange;
    padding: 15px 25px;
    margin-right: 15px;
    color: white;

    &:hover{
        background-color: $orange-light;
    }
}
/* sezione news */
</style>