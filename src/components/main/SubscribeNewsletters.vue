<template>
    <section class="subscribe-newsletters">
        <div class="container">
            <!-- Div che limita la grandezza del contenuto -->
            <div class="text-center mb-5 w-50 mx-auto position-relative">
                <h2 class="display-5 fw-semibold mb-4">Subscribe <span class="text-primary fw-light">Newsletters</span></h2>
                <p class="mb-5 grey-text">Enter your email address to register to our newsletter subscription delivered on a regular basis!</p>
                <div class="input-group">
                    <input type="text" class="form-control my-input small-text" placeholder="Enter your email" aria-label="Enter your email" aria-describedby="submit-email">
                    <button class="btn btn-primary rounded-end" type="button" id="submit-email">Subscribe</button>
                </div>
                <!-- Cerchio verde sulla sinistra -->
                <div class="random-circle"></div>  
                <!-- Semicerchi sulla destra -->
                <div class="spinning-random-circles">
                    <img src="img/shape-spinning-circles.png" alt="">
                </div> 
                <!-- Puntini sulla destra -->
                <div class="skewed-dots">
                    <img src="img/shape-dots-skewed.png" alt="">
                </div> 
            </div>
        </div>
    </section>
</template>

<script>
    export default {

    }
</script>


<style lang="scss">
    .subscribe-newsletters {

        .random-circle {
            position: absolute;
            top: 50%;
            left: -28rem;
            width: 4rem;
            height: 4rem;
            border-radius: 50%;
            border: 0.5rem solid #8FD6CA;
        }
        .spinning-random-circles {
            position: absolute;
            bottom: 10%;
            right: -20rem;
        }
        .skewed-dots {
            position: absolute;
            bottom: 25%;
            right: -20rem;
        }
    }
</style>