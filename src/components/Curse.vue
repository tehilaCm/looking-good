<template>
    <div class="curse">
        <div class="curse-img">
            <img :src="getSrc(img)">
        </div>
        <p class="curse-name">
            {{name}}
        </p>
    </div>
</template>

<script>
export default {
  name: "Curse", 
  props: ['img', 'name'],
  methods: {
        getSrc(name) {
            var images = require.context('../assets/', false, /\.jpg$/);
            return images('./' + name + ".jpg")
        }
    }
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

p{
    font-size: 1.1rem;
}
  
</style>

