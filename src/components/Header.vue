<template>
    <header class="py-4">
        <!-- Contenitore -->
        <div class="container h-100">
            <div class="d-flex justify-content-between align-items-center header_top">
                <!-- Logo -->
                <div class="logo">
                    <a href="/">
                        <img src="../assets/img/logo_seo_w_1x.png" alt="Logo AvadaSeo">
                    </a>
                </div>
                <!-- /Logo -->

                <!-- Barra di navigazione -->
                <nav>
                    <Links :link="links"/>
                </nav>
                <!-- /Barra di navigazione -->
            </div>
            <!-- Contenitore Titolo -->
            <div class="w-50 my_container">
                <div class="title_header">
                    <h1>SEM Campaigns Made Simple With Avada</h1>
                    <p class="py-3">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptate, sint dignissimos ab odio voluptates consequatur perferendis.</p>
                    <span class="btn_orange">Buy avada now</span>
                    <span class="btn_blue">Cuntact US</span>
                </div>
            </div>
            <!-- /Contenitore Titolo -->
        </div>
        <!-- /Contenitore -->
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
@import "../assets/style/globali.scss";

header {
    height: 850px;
    background-image: url("../assets/img/1-hero-image.png");
    background-position: center center;
    background-size: cover;
    background-repeat: no-repeat;
    color: white;
}

.header_top {
    height: 80px;
    line-height: 40px;
}

.my_container {
    height: calc(100% - 80px);
    position: relative;

    .title_header{
        position: absolute;
        top:40%;
        transform: translateY(-40%);

        h1 {
            font-size: 60px;
            font-weight: 600;
        }

        p {
            font-size: 20px;
        }
        .btn_orange {
            @include btn_orange;
            padding: 15px 25px;
            margin-right: 15px;

            &:hover{
                background-color: $orange-light;
            }
        }
        .btn_blue{
            @include btn_blue;

            &:hover{
                background-color: $blue-light;
            }
        }
    }
}

</style>