<template>
    <section class="work-culture">
        <div class="row justify-content-around">
            <!-- Blocco di testo "Learn about our culture at MaxCoach" sulla sinistra -->
            <div class="col-4">
                <div class="text-uppercase mb-3">Everything in <span class="fw-semibold">MaxCoach</span></div>
                <h2 class="display-5 fw-semibold mb-3">Learn about our <span class="text-primary fw-light">Work Culture</span> at MaxCoach</h2>
                <p class="small-text mb-4">Spend some time to visit our website or head office and discover our current courses, enrollment procedure, and registration deadline. We're opening new classes every beginning of each month.</p>
                <span>Have questions? </span>
                <a href="#" class="text-primary fw-semibold">Get Free Guide <i class="fa-solid fa-arrow-right-long"></i></a>
            </div>
            <!-- Immagine del team sulla destra con tutte le immagini svolazzanti -->
            <div class="col-6 floating-imgs-container">
                <!-- Immagine del team -->
                <img class="rounded" src="../../../public/img/stock-full-hd-10.jpg" alt="">
                <!-- Cerchio arancione sulla sinistra -->
                <div class="random-circle"></div>
                <!-- Puntini che spuntano dietro l'immagine della ragazza al pc -->
                <div class="random-dots">
                    <img src="../../../public/img/maxcoach-shape-07.png" alt="">
                </div>
                <!-- Immagine della ragazza al pc -->
                <div class="girl-working-img">
                    <img class="rounded" src="../../../public/img/about-us.jpg" alt="">
                </div>
                <!-- Semicerchi sulla destra -->
                <div class="spinning-random-circles">
                    <img src="../../../public/img/maxcoach-shape-02.png" alt="">
                </div>
            </div>
        </div>
        <!-- Display dei dati sui corsi -->
        <div class="data-display row justify-content-center gx-0 text-center">
            <div class="col-3">
                <div class="text-primary fw-bold display-5">129+</div>
                <span class="fw-semibold text-uppercase">Enrolled learners</span>
            </div>
            <div class="col-3">
                <div class="text-primary fw-bold display-5">80</div>
                <span class="fw-semibold text-uppercase">Finished sessions</span>
            </div>
            <div class="col-3">
                <div class="text-primary fw-bold display-5">4%</div>
                <span class="fw-semibold text-uppercase">Satisfaction rate</span>
            </div>
        </div>
    </section>
</template>

<script>
    export default {

    }
</script>

<style lang="scss">
    .work-culture {
        
        a {
            border-bottom: 1px solid inherit;
        }
        p {
            line-height: 1.5rem;
        }
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
        .data-display {
            margin-top: 7rem;
        }
    }
</style>