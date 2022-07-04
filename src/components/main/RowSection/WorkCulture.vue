<template>
    <!-- Immagine del team sulla destra con tutte le immagini svolazzanti -->
    <div class="col-6 floating-imgs-container">
        <!-- Immagine del team -->
        <img class="rounded" src="img/work-culture.jpg" alt="">
        <!-- Cerchio arancione sulla sinistra -->
        <div class="random-circle"></div>
        <!-- Puntini che spuntano dietro l'immagine della ragazza al pc -->
        <div class="random-dots">
            <img src="img/shape-dots.png" alt="">
        </div>
        <!-- Immagine della ragazza al pc -->
        <div class="girl-working-img">
            <img class="rounded" src="img/girl-pc.jpg" alt="">
        </div>
        <!-- Semicerchi sulla destra -->
        <div class="spinning-random-circles">
            <img src="img/shape-spinning-circles.png" alt="">
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

        .random-circle {
            position: absolute;
            top: -1rem;
            left: -6rem;
            width: 4rem;
            height: 4rem;
            border-radius: 50%;
            border: 0.5rem solid #ECC5AB;
        }
        .random-dots {
            position: absolute;
            top: -4rem;
            right: 5rem;
            z-index: -1;
        }
        .girl-working-img {
            position: absolute;
            top: 0;
            right: 0;
            transform: translate(0, -50%);
        }
        .spinning-random-circles {
            position: absolute;
            bottom: -6rem;
            right: 20%;
        }
    }
</style>