<template>
    <div class="solar-system">
        <div class="sun"><img src="https://png.icons8.com/color/50/000000/sun-star.png"></div>
        <div class="mercury"><img src="https://png.icons8.com/color/50/000000/mercury-planet.png"></div>
    </div>
</template>

<script>
    export default {
        name: "SolarSystem"
    }
</script>

<style scoped>
    @keyframes sun {
        from {
            transform: rotate(0deg);
        }
        to {
            transform: rotate(360deg);
        }
    }
    @keyframes mercury {
        from {
            transform: rotate(0deg) translate(-50px) rotate(0deg);
        }
        to {
            transform: rotate(360deg) translate(-50px) rotate(-720deg);
        }
    }
    .solar-system {
        height: calc(100vh - 16px);
        background-color: #1c1c1c;
        display: flex;
    }
    .sun {
        display: flex;
        position: absolute;
        top: calc(50% - 25px);
        left: calc(50% - 25px);
        margin: auto;
        animation-name: sun;
        animation-duration: 3s;
        animation-iteration-count: infinite;
        animation-timing-function: linear;
    }
    .mercury {
        display: flex;
        position: absolute;
        top: calc(50% - 5px);
        left: calc(50% - 5px);
        margin: auto;
        animation-name: mercury;
        animation-duration: 10s;
        animation-iteration-count: infinite;
        animation-timing-function: linear;
    }
    .mercury img {
        width: 10px;
        height: 10px;
    }
</style>