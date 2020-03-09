<template>
  <div class="home">
    <Slider></Slider>
    <Footer></Footer>
  </div>
</template>

<script>

import Slider from "@/components/Slider.vue";
import Footer from "@/components/Footer.vue";

export default {
  
  name: "Home",
  components: {
    Slider,
    Footer      
  }
};
</script>
