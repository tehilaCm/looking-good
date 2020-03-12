<template>
    <div class="curse">
        <div class="curse-img">
            <img :src="img">
        </div>
        <p class="curse-name">
            {{name}}
        </p>
    </div>
</template>

<script>
export default {
  name: "Curse", 
  props: ['img', 'name']
  
}
</script>

<style scoped>

.curse{
    display: inline-block;
    margin: 2rem;
}

img{
    width: 20rem;
    height: 13.5rem;
}
  
</style>

