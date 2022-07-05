<template>
    <div class="courses-slider">
        <!-- Row che mostra 3 corsi alla volta in base alla pagina corrente -->
        <div class="row row-cols-3 gx-4 mb-3">
            <ItemCard v-for="(course, i) in currentPageCourses" :key="i" :item-info="course"/>
        </div>
        <!-- Flex che stampa i bottoni per le pagine dello slider -->
        <div class="d-flex justify-content-center align-items-center">
            <div v-for="i in Math.ceil(courses.length / 3)" :key="i" class="p-2">
                <div class="page-circle" :class="i === currentPage ? `active` : ``" @click="changeCurrentPage(i)"></div>
            </div>
        </div>
    </div>
</template>

<script>
    import ItemCard from "../ItemCard.vue"

    export default {
        components: {
            ItemCard
        },
        data() {
            return {
                currentPage: 1,
                // Creo un array di array di oggetti. Ogni oggetto rappresenta un corso ed è contenuto in un array che rappresenta la pagina dello slider
                courses: [
                    {
                        type: "course",
                        img_src: "img/course-00.jpg",
                        price: 40.00,
                        title: "Learning to Write as a Professional Author",
                        lessonsNumber: "20",
                        studentsNumber: "50"
                    },
                    {
                        type: "course",
                        img_src: "img/course-01.jpg",
                        price: 0.00,
                        title: "Customer-centric Info-Tech Strategies",
                        lessonsNumber: "24",
                        studentsNumber: "769"
                    },
                    {
                        type: "course",
                        img_src: "img/course-02.jpg",
                        price: 19.00,
                        title: "Open Programming Courses for Everyone: Phyton",
                        lessonsNumber: "17",
                        studentsNumber: "62"
                    },
                    {
                        type: "course",
                        img_src: "img/course-03.jpg",
                        price: 0.00,
                        title: "Test",
                        lessonsNumber: "20",
                        studentsNumber: "50"
                    },
                    {
                        type: "course",
                        img_src: "img/course-03.jpg",
                        price: 0.99,
                        title: "Super cheap course",
                        lessonsNumber: "24",
                        studentsNumber: "769"
                    },
                    {
                        type: "course",
                        img_src: "img/course-03.jpg",
                        price: 19.00,
                        title: "Open Programming Courses for Everyone: Phyton",
                        lessonsNumber: "17",
                        studentsNumber: "62"
                    },
                    {
                        type: "course",
                        img_src: "img/course-00.jpg",
                        price: 40.00,
                        title: "Learning to Write as a Professional Author",
                        lessonsNumber: "20",
                        studentsNumber: "50"
                    },
                    {
                        type: "course",
                        img_src: "img/course-01.jpg",
                        price: 0.00,
                        title: "Customer-centric Info-Tech Strategies",
                        lessonsNumber: "24",
                        studentsNumber: "769"
                    }
                ]
            }
        },
        computed: {
            // Restituisce i corsi della pagina corrente
            currentPageCourses() {
                return this.courses.slice(3 * this.currentPage - 3, 3 * this.currentPage);
            }
        },
        methods: {
            // Cambia pagina al click su un punto
            changeCurrentPage(i) {
                this.currentPage = i;
            }
        }
    }
</script>

<style lang="scss">
    .courses-slider {
        width: 90%;
        margin: auto;

        .page-circle {
            width: 0.5rem;
            height: 0.5rem;
            border-radius: 50%;
            background: #D8D8D8;

            &.active {
                width: 0.8rem;
                height: 0.8rem;
                background: black;
            }
        }
    }
</style>