<template>
    <!-- Immagine della ragazza con tutte le immagini svolazzanti -->
    <div class="col-6 floating-imgs-container">
        <!-- Immagine dei 4 nei riquadri -->
        <img class="rounded" src="img/transform-you.png" alt="">
        <!-- Linee in basso a destra -->
        <div class="random-lines">
            <img src="img/shape-lines.png" alt="">
        </div>
        <!-- Puntini in cerchio -->
        <div class="random-dots-circle">
            <img src="img/shape-dots-circle.png" alt="">
        </div>
        <!-- Cerchio random sulla destra -->
        <div class="random-circle"></div>
        <!-- Puntini in basso -->
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

        .random-lines {
            position: absolute;
            bottom: 2rem;
            left: -18rem;
        }
        .random-dots-circle {
            position: absolute;
            top: 8rem;
            left: -6rem;
            z-index: -1;
        }
        .random-circle {
            position: absolute;
            top: -2rem;
            right: -9rem;
            width: 4rem;
            height: 4rem;
            border-radius: 50%;
            border: 0.5rem solid #ECC5AB;
        }
        .random-dots {
            position: absolute;
            bottom: -6rem;
            right: 16rem;
            z-index: -1;
        }
    }
</style>