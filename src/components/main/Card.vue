<template>
    <div>
        <i :class="icon"></i>
        <h3 class="fw-bold">{{ title }}</h3>
        <p>{{ text }}</p>
        <a v-show="link"
            href="#">{{ link }}</a>
    </div>
</template>

<script>
export default {
    name:"Card",
    props: {
        icon: String,
        title: String,
        text: String,
        link: String
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/globali.scss";

h3:hover {
    color: $orange;
}

i {
    margin-bottom: 25px;
    font-size: 30px;
    color: $orange;
}

a {
    text-decoration: none;
    color: $orange;
    &:hover {
        color: $orange;
    }
}

a::after {
    content: '\203A';
    font-size: 20px;
    padding-left: 5px;
}


</style>