<template>
    <div>
        <div class="course-card bg-white rounded">
            <!-- Immagine corso -->
            <img :src="`img/course-${courseInfo.img_src}`" :alt="`Immagine del corso ${courseInfo.title}`">
            <div class="p-4">
                <!-- Prezzo -->
                <div class="fw-bold mb-3">
                    <span class="fs-4 text-primary">${{priceToInt}}</span>
                    <span class="text-primary">.{{priceDecimals}}</span>
                </div>
                <!-- Titolo -->
                <h5 class="fw-semibold mb-4">{{courseInfo.title}}</h5>
                <!-- Numero Lezioni e studenti -->
                <div class="small-text grey-text mb-3">
                    <span class="d-inline-block me-5"><i class="fa-regular fa-file-lines"></i> {{courseInfo.lessonsNumber}} Lessons</span>
                    <span class="d-inline-block"><i class="fa-regular fa-user"></i> {{courseInfo.studentsNumber}} Student</span>
                </div>
            </div>
            <span v-if="isFree" class="my-badge ps-4 pe-3 py-2 text-white text-uppercase fw-bold">Free</span>
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            courseInfo: Object
        },
        computed: {
            priceToInt() {
                return parseInt(this.courseInfo.price);
            },
            priceDecimals() {
                return (this.courseInfo.price % 1).toFixed(2).toString().split('.')[1];
            },
            isFree() {
                return this.courseInfo.price === 0;
            }
        }
    }
</script>

<style lang="scss">
    .course-card {
        overflow: hidden;
        position: relative;

        img {
            width: 100%;
        }

        .my-badge {
            background: #EE7455;
            position: absolute;
            top: 0;
            right: 0;
            clip-path: polygon(0 0, 100% 0, 100% 100%, 0% 100%, 15% 55%, 15% 45%);
        }
    }
</style>