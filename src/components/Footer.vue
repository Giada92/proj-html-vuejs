<template>
  <footer class="text-center py-4">
    <img src="../assets/img/logo_seo_1x.png" alt="Logo AvadaSeo">
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
  </footer>
</template>

<script>


export default {
    name: "Footer",
    props: {
      links: Array
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

footer {
  height: 500px;
}

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

</style>