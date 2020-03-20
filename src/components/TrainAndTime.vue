<template>
    <div class="trainAndTime">
        <div class="train">{{train}}</div>
        <div class="time">{{time}}</div>
    </div>
</template>

<script>
export default {
    name: "TimeAndTrain",
    props: ['train', 'time']
};
</script>

<style scoped>

    *{
        font-weight: bold;
    }

    .trainAndTime{
        border-bottom: 1px solid black;
        margin: 1rem 0;
    }

    .train{
        display: inline-block;
        width: calc(100% - 6rem);
        text-align: right;
    }

    .time{
        display: inline-block;
        width: 6rem;
        text-align: right;
    }

</style>