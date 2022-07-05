<template>
    <div>
        <div class="item-card" :class="itemInfo.type === `course` ? `bg-white rounde` : ``">
            <!-- Immagine corso -->
            <img :src="itemInfo.img_src" :alt="itemInfo.title">
            <div class="p-4">
                <!-- Corsi -->
                <div v-if="itemInfo.type === `course`">
                    <!-- Prezzo -->
                    <div class="fw-bold mb-3">
                        <span class="fs-4 text-primary">${{priceToInt}}</span>
                        <span class="text-primary">.{{priceDecimals}}</span>
                    </div>
                    <!-- Titolo -->
                    <h5 class="fw-semibold mb-4">{{itemInfo.title}}</h5>
                    <!-- Numero Lezioni e studenti -->
                    <div class="small-text grey-text mb-3">
                        <span class="d-inline-block me-5"><i class="fa-regular fa-file-lines"></i> {{itemInfo.lessonsNumber}} Lessons</span>
                        <span class="d-inline-block"><i class="fa-regular fa-user"></i> {{itemInfo.studentsNumber}} Student</span>
                    </div>
                </div>
                <!-- Blog -->
                <div v-if="itemInfo.type === `blog`">
                    <!-- Categoria -->
                    <span class="text-uppercase grey-text">${{itemInfo.category}}</span>
                    <!-- Titolo -->
                    <h5 class="fw-semibold mb-4">{{itemInfo.title}}</h5>
                    <!-- Data e numero visualizzazioni -->
                    <div class="small-text grey-text mb-3">
                        <span class="d-inline-block me-5"><i class="fa-regular fa-calendar"></i> {{itemInfo.date}}</span>
                        <span class="d-inline-block"><i class="fa-solid fa-eye"></i> {{itemInfo.viewCount}} views</span>
                    </div>
                </div>
            </div>
            <span v-if="isFree" class="my-badge ps-4 pe-3 py-2 text-white text-uppercase fw-bold">Free</span>
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            itemInfo: Object
        },
        computed: {
            priceToInt() {
                return parseInt(this.itemInfo.price);
            },
            priceDecimals() {
                return (this.itemInfo.price % 1).toFixed(2).toString().split('.')[1];
            },
            isFree() {
                return this.itemInfo.price === 0;
            }
        }
    }
</script>

<style lang="scss">
    .item-card {
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