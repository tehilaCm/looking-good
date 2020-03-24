<template>
    <div class="coach">
        <div class="coach-img">
            <figure><img :src="img"></figure>
        </div>
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

        /* Gray Scale */
    .coach-img figure img {
        -webkit-filter: grayscale(100%);
        filter: grayscale(100%);
        -webkit-transition: .3s ease-in-out;
        transition: .3s ease-in-out;
    }
    .coach-img figure:hover img {
        -webkit-filter: grayscale(0);
        filter: grayscale(0);
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