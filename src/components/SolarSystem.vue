<template>
    <div class="solar-system">
        <div class="btn-panel">
            <input title="speed" v-on:input="changeSpeed" v-model="speed" type="range" min="1" max="250" step="1"/>
        </div>
        <div class="sun"><img src="../assets/planets/sun-star.png" alt="sun"></div>
        <div class="sun2"><img src="../assets/planets/sun-star.png" alt="sun"></div>
        <div class="mercury"><img src="../assets/planets/mercury-planet.png" alt="mercury"></div>
        <div class="mercury-path"></div>
        <div class="venus"><img src="../assets/planets/venus-planet.png" alt="venus"></div>
        <div class="venus-path"></div>
        <div class="earth"><img src="../assets/planets/globe.png" alt="earth"></div>
        <div class="earth-path"></div>
        <div class="mars"><img src="../assets/planets/mars-planet.png" alt="mars"></div>
        <div class="mars-path"></div>
        <div class="jupiter"><img src="../assets/planets/jupiter-planet.png" alt="jupiter"></div>
        <div class="jupiter-path"></div>
        <div class="saturn"><img src="../assets/planets/saturn-planet.png" alt="saturn"></div>
        <div class="saturn-path"></div>
        <div class="uranus"><img src="../assets/planets/uranus-planet.png" alt="uranus"></div>
        <div class="uranus-path"></div>
        <div class="neptune"><img src="../assets/planets/neptune-planet.png" alt="neptune"></div>
        <div class="neptune-path"></div>
<!--        <planet img="https://img.icons8.com/color/50/000000/mercury-planet.png"></planet>-->
    </div>
</template>

<script>
    import Planet from "@/components/Planet";
    export default {
        name: "SolarSystem",
        components: {Planet},
        data() {
            return {
                speed: 0
            }
        },
        mounted() {
            // this.changeSpeed();
        },
        methods: {
            changeSpeed() {
                document.getElementsByClassName('mercury')[0].style.animationDuration = (8.8 / this.speed) + 's';
                document.getElementsByClassName('venus')[0].style.animationDuration = (22.5 / this.speed) + 's';
                document.getElementsByClassName('earth')[0].style.animationDuration = (36.5 / this.speed) + 's';
                document.getElementsByClassName('mars')[0].style.animationDuration = (68.7 / this.speed) + 's';
                document.getElementsByClassName('jupiter')[0].style.animationDuration = (432.9 / this.speed) + 's';
                document.getElementsByClassName('saturn')[0].style.animationDuration = (1075.3 / this.speed) + 's';
                document.getElementsByClassName('uranus')[0].style.animationDuration = (3066 / this.speed) + 's';
                document.getElementsByClassName('neptune')[0].style.animationDuration = (6014.8 / this.speed) + 's';
            }
        }
    }
</script>

<style scoped>
    @keyframes sun {
        from {
            transform: rotate(0deg);
        }
        to {
            transform: rotate(180deg);
        }
    }
    @keyframes sun2 {
        from {
            transform: rotate(0deg);
        }
        to {
            transform: rotate(-180deg);
        }
    }
    @keyframes mercury {
        from {
            transform: rotate(0deg) translate(-48px) rotate(0deg);
        }
        to {
            transform: rotate(-360deg) translate(-48px) rotate(-738deg);
        }
    }
    @keyframes venus {
        from {
            transform: rotate(0deg) translate(-88px) rotate(0deg);
        }
        to {
            transform: rotate(-360deg) translate(-88px) rotate(539deg);
        }
    }
    @keyframes earth {
        from {
            transform: rotate(0deg) translate(-120px) rotate(0deg);
        }
        to {
            transform: rotate(-360deg) translate(-120px) rotate(-13140deg);
        }
    }
    @keyframes mars {
        from {
            transform: rotate(0deg) translate(-168px) rotate(0deg);
        }
        to {
            transform: rotate(-360deg) translate(-168px) rotate(-11945deg);
        }
    }
    @keyframes jupiter {
        from {
            transform: rotate(0deg) translate(-288px) rotate(0deg);
        }
        to {
            transform: rotate(-360deg) translate(-288px) rotate(360deg);
        }
    }
    @keyframes saturn {
        from {
            transform: rotate(0deg) translate(-348px) rotate(0deg);
        }
        to {
            transform: rotate(-360deg) translate(-348px) rotate(360deg);
        }
    }
    @keyframes uranus {
        from {
            transform: rotate(0deg) translate(-390px) rotate(0deg);
        }
        to {
            transform: rotate(-360deg) translate(-390px) rotate(360deg);
        }
    }
    @keyframes neptune {
        from {
            transform: rotate(0deg) translate(-448px) rotate(0deg);
        }
        to {
            transform: rotate(-360deg) translate(-448px) rotate(0deg);
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
    .sun img {
        width: 50px;
        height: 50px;
    }
    .sun2 {
        display: flex;
        position: absolute;
        top: calc(50% - 25px);
        left: calc(50% - 25px);
        margin: auto;
        animation-name: sun2;
        animation-duration: 3s;
        animation-iteration-count: infinite;
        animation-timing-function: linear;
    }
    .sun2 img {
        width: 50px;
        height: 50px;
    }
    .mercury {
        display: flex;
        position: absolute;
        top: calc(50% - 5px);
        left: calc(50% - 5px);
        margin: auto;
        animation-name: mercury;
        animation-duration: 8.8s;
        animation-iteration-count: infinite;
        animation-timing-function: linear;
    }
    .mercury img {
        width: 10px;
        height: 10px;
    }
    .venus {
        display: flex;
        position: absolute;
        top: calc(50% - 8px);
        left: calc(50% - 8px);
        margin: auto;
        animation-name: venus;
        animation-duration: 22.5s;
        animation-iteration-count: infinite;
        animation-timing-function: linear;
    }
    .venus img {
        width: 16px;
        height: 16px;
    }
    .earth {
        display: flex;
        position: absolute;
        top: calc(50% - 9px);
        left: calc(50% - 9px);
        margin: auto;
        animation-name: earth;
        animation-duration: 36.5s;
        animation-iteration-count: infinite;
        animation-timing-function: linear;
    }
    .earth img {
        width: 18px;
        height: 18px;
    }
    .mars {
        display: flex;
        position: absolute;
        top: calc(50% - 6px);
        left: calc(50% - 6px);
        margin: auto;
        animation-name: mars;
        animation-duration: 68.7s;
        animation-iteration-count: infinite;
        animation-timing-function: linear;
    }
    .mars img {
        width: 12px;
        height: 12px;
    }
    .jupiter {
        display: flex;
        position: absolute;
        top: calc(50% - 15px);
        left: calc(50% - 15px);
        margin: auto;
        animation-name: jupiter;
        animation-duration: 432.9s;
        animation-iteration-count: infinite;
        animation-timing-function: linear;
    }
    .jupiter img {
        width: 30px;
        height: 30px;
    }
    .saturn {
        display: flex;
        position: absolute;
        top: calc(50% - 15px);
        left: calc(50% - 15px);
        margin: auto;
        animation-name: saturn;
        animation-duration: 1075.3s;
        animation-iteration-count: infinite;
        animation-timing-function: linear;
    }
    .saturn img {
        width: 30px;
        height: 30px;
    }
    .uranus {
        display: flex;
        position: absolute;
        top: calc(50% - 13px);
        left: calc(50% - 13px);
        margin: auto;
        animation-name: uranus;
        animation-duration: 3066s;
        animation-iteration-count: infinite;
        animation-timing-function: linear;
    }
    .uranus img {
        width: 26px;
        height: 26px;
    }
    .neptune {
        display: flex;
        position: absolute;
        top: calc(50% - 8px);
        left: calc(50% - 8px);
        margin: auto;
        animation-name: neptune;
        animation-duration: 6014.8s;
        animation-iteration-count: infinite;
        animation-timing-function: linear;
    }
    .neptune img {
        width: 16px;
        height: 16px;
    }
</style>
