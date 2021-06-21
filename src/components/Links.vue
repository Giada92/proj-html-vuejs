<template>
    <ul class="d-flex justify-content-around mt-4">
        <li class="px-4"
            @click="changeNavStatus(index)"
            v-for="el, index in link" :key="index">
            <a href="el.link" :class="{active: index==activeIndex}">
                {{ el.text }} 
                <span class="badge my_badge">{{ el.text2 }}</span>
            </a>
        </li>
    </ul>
</template>

<script>
export default {
    name: "Links",
    props: {
        link: Array
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
        font-weight: 600;
        font-size: 16px;
        vertical-align: middle;
        list-style: none;
        cursor: pointer;

        a {
            text-decoration: none;
            color: white;
            &:hover,
            &.active {
                color: $orange;
            }
        }

        &:last-child {
            padding: 0 30px;
            @include btn_orange;
        }
        &:last-child:hover {
            background-color: $orange-light;
        }
         &:last-child:hover a{
            color: white;
        }

        .my_badge {
            margin-left: 5px;
            font-weight: 400;
            //vertical-align: super;
            border: 1px solid $orange;
            color: $orange;
            text-transform: uppercase;
        }
    }
}

</style>