<template>
    <main>
        <div class="container">
            <section class="work-culture">
                <div class="row justify-content-around">
                    <div class="col-4">
                        <div class="text-uppercase mb-3">Everything in <span class="fw-semibold">MaxCoach</span></div>
                        <h2 class="display-5 fw-semibold mb-3">Learn about our <span class="text-primary fw-light">Work Culture</span> at MaxCoach</h2>
                        <p class="small-text mb-4">Spend some time to visit our website or head office and discover our current courses, enrollment procedure, and registration deadline. We're opening new classes every beginning of each month.</p>
                        <span>Have questions? </span>
                        <a href="#" class="text-primary fw-semibold">Get Free Guide <i class="fa-solid fa-arrow-right-long"></i></a>
                    </div>
                    <div class="col-6 floating-imgs-container">
                        <img src="../../public/img/stock-full-hd-10.jpg" alt="Teamwork">
                        <div class="random-circle"></div>
                        <div class="random-dots">
                            <img src="../../public/img/maxcoach-shape-07.png" alt="">
                        </div>
                        <div class="girl-working-img">
                            <img class="rounded" src="../../public/img/about-us.jpg" alt="Ragazza al pc">
                        </div>
                        <div class="spinning-random-circles">
                            <img src="../../public/img/maxcoach-shape-02.png" alt="">
                        </div>
                    </div>
                </div>
            </section>
        </div>
    </main>
</template>

<script>
    export default {

    }
</script>

<style lang="scss">
    main {
        padding-top: 10rem;
        padding-bottom: 5rem;

        .work-culture {
            a {
                border-bottom: 1px solid inherit;
            }
            p {
                line-height: 1.5rem;
            }
            .floating-imgs-container{
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
        }
    }
</style>