<template>
    <header class="py-4">
        <div class="container d-flex justify-content-between align-items-center header_top">
            <div class="logo">
                <a href="/">
                    <img src="../assets/img/logo_seo_w_1x.png" alt="Logo AvadaSeo">
                </a>
            </div>
            <nav>
                <Links :link="links"/>
            </nav>
        </div>
    </header>
</template>

<script>
import Links from './Links.vue';

export default {
    name:"Header",
    components:{
        Links
    },
    props: {
        links: Array
    }
}
</script>

<style lang="scss" scoped>

header {
    height: 850px;
    background-image: url("../assets/img/1-hero-image.png");
    background-position: center center;
    background-size: cover;
    background-repeat: no-repeat;
}

.header_top {
    height: 80px;
    line-height: 40px;
}

</style>