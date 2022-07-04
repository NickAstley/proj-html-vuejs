<template>
    <!-- Immagine della ragazza con tutte le immagini svolazzanti -->
    <div class="col-6 floating-imgs-container">
        <!-- Immagine della ragazza che prende appunti -->
        <img class="rounded" src="img/upgrade-life.jpg" alt="">
        <!-- Logo di YouTube -->
        <div class="youtube-logo">
            <img src="img/icon-youtube-play.png" alt="">
        </div>
        <!-- Puntini in cerchio -->
        <div class="random-dots-circle">
            <img src="img/shape-dots-circle.png" alt="">
        </div>
        <!-- Cerchio random sulla destra -->
        <div class="random-circle"></div>
        <!-- Puntini in basso a destra -->
        <div class="random-dots">
            <img src="img/shape-dots.png" alt="">
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
    .floating-imgs-container {
        position: relative;

        .youtube-logo {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(calc(-50% + 22px), -50%);
        }
        .random-dots-circle {
            position: absolute;
            top: 3rem;
            left: -6rem;
            z-index: -1;
        }
        .random-circle {
            position: absolute;
            top: -2rem;
            right: -11rem;
            width: 4rem;
            height: 4rem;
            border-radius: 50%;
            border: 0.5rem solid #ECC5AB;
        }
        .random-dots {
            position: absolute;
            bottom: -6rem;
            right: -2rem;
            z-index: -1;
        }
    }
</style>