<template>
    <div class="coach">
        <div class="coach-img">
            <figure><img :src="img"></figure>
        </div>

        <!-- <figure class="imghvr-fade">
        <img :src="img">
        <figcaption>
            // Hover Content
        </figcaption>
        </figure> -->

        <div class="coach-details">
            <h2 class="name">{{name}}</h2>
            <p class="description">{{description}}</p>
        </div>
    </div>
</template>


<script>
export default {
    name: "Coach",
    props: ['img', 'name', 'description']
};
</script>

<style scoped>

    .coach{
        width: fit-content;
        margin: 2rem 1rem;
    }

    img{
        border-radius: 50%;
        width: 17rem;
        height: 17rem;
    }

    .coach-details{
        width: 17rem;
    }

    h2{
        font-size: 2rem;
    }

    .coach-img figure {
        position: relative;
    }
    .coach-img figure::before {
        position: absolute;
        top: 50%;
        left: 50%;
        z-index: 2;
        display: block;
        content: '';
        width: 0;
        height: 0;
        background: rgba(255,255,255,.2);
        border-radius: 100%;
        -webkit-transform: translate(-50%, -50%);
        transform: translate(-50%, -50%);
        opacity: 0;
    }
    .coach-img figure:hover::before {
        -webkit-animation: circle .75s;
        animation: circle .75s;
    }
    @-webkit-keyframes circle {
        0% {
            opacity: 1;
        }
        40% {
            opacity: 1;
        }
        100% {
            width: 200%;
            height: 200%;
            opacity: 0;
        }
    }
    @keyframes circle {
        0% {
            opacity: 1;
        }
        40% {
            opacity: 1;
        }
        100% {
            width: 200%;
            height: 200%;
            opacity: 0;
        }
    }

    @media (min-width: 51rem)
    {
        .coach{
            margin: 2rem 3.5rem;
        }

        img{
            width: 20rem;
            height: 20rem;
        }

        .coach-details{
            width: 17rem;
        }
    }

</style>