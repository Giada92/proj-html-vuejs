<template>
  <div>
        <div>
            <img :src="clients[imgIndex].url" alt="">
            <h5 class="fst-italic">{{ clients[imgIndex].text }}</h5>
            <p class="fw-bold">{{ clients[imgIndex].testimonials }}, 
                <span class="fw-normal">{{ clients[imgIndex].job }}</span>
            </p>
        </div>
        <nav>
            <i  @click="changeTestimonial(index)"
                v-for="client, index in clients" :key="index" 
                :class="(imgIndex == index)? 'fas fa-circle': 'far fa-circle'"></i>   
        </nav> 
  </div>
</template>

<script>
export default {
    name:"Slider",
    props:{
        clients: Array
    },
    data(){
        return{
            imgIndex: 0,
            autoPlay: ""
        }
    },
    methods:{
        changeTestimonial: function(newIndex) {
            this.imgIndex = newIndex;
        }
    }/* ,
    created: function() {
        this.autoPlay = setInterval(()=>{ 
                this.imgIndex++;
                if(this.imgIndex >= this.clients.length){
                    this.imgIndex = 0;
                }
            }, 5000);
        } */
}
</script>

<style lang="scss" scoped>

img {
    width: 10%;
    border-radius: 50%;
    margin: 30px 0;
}

p,
h5{
    font-size: 22px;
    margin: 10px 0;
}

i {
    padding: 10px 5px;
    font-size: 13px;
    cursor: pointer;
}

</style>