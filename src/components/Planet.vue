<template>
    <div><img :src="img"></div>
</template>

<script>
    export default {
        name: "Planet",
        props: ['radius', 'rotationAxis', 'rotationSun', 'distanceFromTheSun', 'img']
    }
</script>

<style scoped>

</style>