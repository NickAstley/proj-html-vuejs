<template>
    <section class="upgrade-life">
        <div class="row justify-content-around">
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
            <!-- Blocco di testo "Upgrade yours skills, upgrade your life" sulla destraa -->
            <div class="col-4 pt-5">
                <div class="text-uppercase mb-3">How we work</div>
                <h2 class="display-5 fw-semibold mb-3">Upgrade Your Skills <span class="text-primary fw-light">Upgrade Your Life</span></h2>
                <p class="small-text mb-4">Opening up more opportunities in front of you to get the ticket to more enjoyable door in life. Getting equipped with new skills for new sets of insights into your career.<br>MaxCoach accompany learners in every stage of learning.</p>
                <a href="#" class="fw-semibold">Download free guidebook <i class="fa-solid fa-arrow-right-long"></i></a>
            </div>
        </div>
    </section>
</template>

<script>
    export default {

    }
</script>

<style lang="scss">
    @import "../../assets/scss/variables";

    .upgrade-life {

        a {
            border-bottom: 1px solid #696969;

            &:hover {
                border-color: $primary;
            }
        }
        p {
            line-height: 1.5rem;
        }
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
    }
</style>