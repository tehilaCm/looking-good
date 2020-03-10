<template>
    <div class="fling-minislide">
        <img src="../assets/train5.jpg" alt="Slide 4" />
        <img src="../assets/train2.jpg" alt="Slide 3" />
        <img src="../assets/train3.jpg" alt="Slide 2" />
        <img src="../assets/train4.jpg" alt="Slide 1" />
    </div>
</template>

<script>
    export default {
        name: "SwitchImages"
    };
</script>

<style scoped>

    .fling-minislide { 
    position: relative;
    overflow: hidden;
    height: 25rem;
    margin: 0;
    left: 0;
    text-align: left;
    font-size: 0;
    }

.fling-minislide img{ 
    position:absolute;
    animation:fling-minislide 20s infinite;
    opacity:0;
    width: 100%;
    height: 30rem;
    float: left;
}

@keyframes fling-minislide {25%{opacity:1;} 40%{opacity:0;}}
.fling-minislide img:nth-child(4){
    animation-delay:0s;
}
.fling-minislide img:nth-child(3){  
    animation-delay:5s;
}
.fling-minislide img:nth-child(2){
    animation-delay:10s;
}
.fling-minislide img:nth-child(1){
    animation-delay:15s;
}

@media (min-width: 51rem)
{
 .fling-minislide { 
    height: 30rem;
 }
}

</style>