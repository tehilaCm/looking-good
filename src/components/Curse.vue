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

  
</style>

