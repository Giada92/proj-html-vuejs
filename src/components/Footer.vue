<template>
  <footer class="text-center py-4 mt-3">
    <!-- Logo -->
    <a href="#">
      <img src="../assets/img/logo_seo_1x.png" alt="Logo AvadaSeo">
    </a>
    <!-- /Logo -->

    <!-- Elenco menù -->
    <div class="my-5">
      <ul class="d-flex justify-content-center">
        <li 
          @click="changeNavStatus(index)"
          v-for="link, index in links" :key="index">
          <a :class="{active: index==activeIndex}"
            :href="link.link"> {{ link.text }}</a>
        </li>
      </ul>
    </div>
    <!-- /Elenco menù -->

    <!-- contenitore copyright -->
    <div class="my-3">
      <span v-for="el, index in info" :key="index">
        {{ el.name }} <strong>{{ el.by }}</strong> |
      </span>
    </div>
    <!-- /contenitore copyright -->

    <!-- Contenitore icone social -->
    <div class="social my-4">
      <i class="fab fa-facebook-f"></i>
      <i class="fab fa-instagram"></i>
      <i class="fab fa-twitter"></i>
      <i class="fab fa-youtube"></i>
    </div>
    <!-- /Contenitore icone social -->

  </footer>
</template>

<script>


export default {
    name: "Footer",
    props: {
      links: Array,
      info: Array
    },
    data(){
        return{
            activeIndex: 0
        }
    },
    methods: {
        changeNavStatus: function(index){
            return (this.activeIndex = index);
        }
    }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/globali.scss";

ul {
    li {
      padding: 0 20px;
      list-style: none;

      a {
        font-size: 14px;
        font-weight: 600;
        text-decoration: none;
        color: #595959;
        &:hover,
        &.active {
          color: $orange;
        }
      }
    }
}

span:first-child::before{
  content: "\00A9";
}

span {
  font-size: 14px;
  color: #818e9d;
    strong {
      color: black;
    }
}

.social {
    color: #5a5759;

    i {
      display: inline-block;
      font-size: 25px;
      margin: 0 10px;
      cursor: pointer;
      &:hover {
        color: $grey-light;
      }
    }
}

</style>