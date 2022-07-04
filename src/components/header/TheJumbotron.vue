<template>
    <div class="jumbotron row align-items-center g-0">
        <!-- Contenuto principale -->
        <div class="text-white text-center">
            <h2 class="fw-bold">Commence Business</h2>
            <h1 class="display-3 mb-4">Distant Mentoring Program</h1>
            <button class="btn btn-secondary fw-bold px-5 py-3">Download free guidebook <i class="fa-solid fa-arrow-right-long"></i></button>
        </div>
        <!-- Barra laterale con pulsanti -->
        <div class="side-menu bg-white text-center rounded-start">
            <!-- Icona squadra -->
            <div>
                <a href="#" class="clickable">
                    <i class="fa-solid fa-ruler-horizontal"></i>
                </a>
            </div>
            <!-- Icona salvagente -->
            <div>
                <a href="#" class="clickable">
                    <i class="fa-regular fa-life-ring"></i>
                </a>
            </div>
            <!-- Icona libro -->
            <div>
                <a href="#" class="clickable">
                    <i class="fa-solid fa-book"></i>
                </a>
            </div>
            <!-- Icona carrello -->
            <div>
                <a href="#" class="clickable">
                    <i class="fa-solid fa-cart-shopping"></i>
                </a>
            </div>
        </div>
    </div>
</template>

<script>
    export default{

    }
</script>

<style lang="scss">
    @import '../../assets/scss/variables';

    .jumbotron {
        height: 700px;
        background-image: url("../../../public/img/home-3-hero-bg.jpg");
        background-size: cover;
        background-position: center;
        position: relative;

        .side-menu {
            position: absolute;
            top: 120px;
            right: 0;
            width: auto;

            .clickable {
                padding: 0.5rem;
            }
        }
    }
</style>