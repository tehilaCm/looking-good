<template>
    <div class="curse">
        <div class="curse-img">
            <img :src="image-src">
        </div>
        <p class="curse-name">
            {{curse-name}}
        </p>
    </div>
</template>

<script>
export default {
  name: "Curse", 
  data: function() {
    return{
        products: [
        {
            img: "../assets/pilates.png",
            name: "פילאטיס מזרן"
        },
        {
            img: "../assets/pilates.png",
            name: "פילאטיס מזרן"
        },
         {
            img: "../assets/pilates.png",
            name: "פילאטיס מזרן"
        },
         {
            img: "../assets/pilates.png",
            name: "פילאטיס מזרן"
        },
         {
            img: "../assets/pilates.png",
            name: "פילאטיס מזרן"
        },
         {
            img: "../assets/pilates.png",
            name: "פילאטיס מזרן"
        }
      ]
  
    }
},
    methods: {
    
    
        }
}
</script>

<style scoped>

  
</style>

