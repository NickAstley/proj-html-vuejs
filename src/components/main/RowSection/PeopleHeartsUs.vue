<template>
    <!-- Recensione sulla destra -->
    <div class="col-6 position-relative">
        <div class="review-container px-5">
            <h5 class="mb-3">Professional team of specialists and passionate mentors at reach</h5>
            <p class="mb-5">I need to get a certification for English proficiency and MaxCoach is my best choice. Their Tutors are smart and professional when dealing with students.</p>
            <div class="d-flex align-items-center">
                <div>
                    <img class="circle" src="img/testimonial-avatar-01.jpg" alt="Foto di Madley Pondor">
                </div>
                <div class="px-3">
                    <h6 class="fw-bold text-uppercase">Madley Pondor</h6>
                    <span class="small-text">/ IT Specialist</span>
                </div>
            </div>
        </div>
        <!-- Recensione che spunta sopra -->
        <div class="review-container floating-review px-5">
            <h5 class="mb-3">The MaxCoach team works really hard to ensure high level of quality</h5>
            <p class="mb-5">I am happy with their arrangement of lessons and subjects. They</p>
        </div>
        <!-- Recensione che spunta sotto -->
        <div class="review-container floating-review float-below px-5 w-100">
            <div class="d-flex align-items-center">
                <div>
                    <img class="circle" src="img/testimonial-avatar-02.jpg" alt="Foto di Madley Pondor">
                </div>
                <div class="px-3">
                    <h6 class="fw-bold text-uppercase">Mina Hollace</h6>
                    <span class="small-text">/ Freelancer</span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .review-container {
        padding-top: 2rem;
        padding-bottom: 2rem;
        background: white;
        box-shadow: rgba(0, 0, 0, 0.35) 0px 5px 15px;

        .circle {
            border-radius: 50%;
            width: 5rem;
        }
        &.floating-review {
            position: absolute;
            top: -8rem;
            left: 0;
            transform: scale(0.7);
            z-index: -1;
            opacity: 0.5;

            &.float-below {
                top: unset;
                bottom: -6rem;
            }
            h5 {
                line-height: 2rem;
            }
        }
    }
</style>