<template>
    <div>
        {{train}}
        {{time}}
    </div>
</template>

<script>
export default {
    name: TimeAndTrain,
    props: ['train', 'time']
};
</script>