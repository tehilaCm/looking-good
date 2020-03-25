<template>
    <div>
        <figure class="imghvr-flip-diag-2">
            <img :src="getSrc(img)">
            <figcaption>
                <h1 class="name">{{name}}</h1>
                <p class="description">{{description}}</p>
            </figcaption>
        </figure>
    </div>    
</template>

<script>
export default {
    name: "CurseForPage", 
    props: ['img', 'name', 'description'],
    methods: {
        getSrc(name) {
            var images = require.context('../assets/', false, /\.jpg$/);
            return images('./' + name + ".jpg")
        }
    }
}
</script>

<style scoped>

    div{
        margin: 0.1rem auto;
    }

    img{
        width: 100%;
        height: 15rem;
        margin: 0; 
    }

    figure, figcaption{
        background-color: rgb(219, 134, 236);;
    }

    figure{
        width: 98%;
    }

    figcaption{
        padding: 1rem;
    }

    h1{
        font-size: 2.5rem;
    }

    p{
        font-size: 1.1rem;
    }

    @media (min-width: 33rem)
    {
        div{
            margin: 1.5rem auto;
        }

        img{
            height: 20rem;
        }

        figure{
            width: 90%;
            box-shadow: 1px 2px 5px grey;
        }

        figcaption{
            padding: 3.5rem;
        }

        h1{
            font-size: 2.5rem;
        }

        p{
            font-size: 1.2rem;
        }
    }

    @media(min-width: 51rem)
    {
        div{
            width: 45%;
        }

        figure{
            width: 100%;
        }

        figcaption{
            padding: 1.5rem;
        }
    }

</style>