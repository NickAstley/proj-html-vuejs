<template>
    <section class="last-courses">
        <div class="container">
            <!-- Blocco con titolo -->
            <div class="text-center mb-5">
                <div class="text-uppercase mb-3 grey-text">Join MaxCoach at best</div>
                <h2 class="display-5 fw-semibold mb-3">Last Online <span class="text-primary fw-light">Courses</span></h2>   
            </div>
            <!-- Slider dei corsi -->
            <CoursesSlider class="mb-5"/>
            <!-- Info sulle notifiche sui corsi -->
            <div class="w-50 mx-auto text-center">
                <span>Control your personal preference settings to get notified about appropriate courses. </span>
                <a href="#" class="fw-semibold">View all courses <i class="fa-solid fa-arrow-right-long"></i></a>
            </div>
        </div>
    </section>
</template>

<script>
    import CoursesSlider from "./LatestCourses/CoursesSlider"

    export default {
        components: {
            CoursesSlider
        }
    }
</script>

<style lang="scss">
    @import "../../assets/scss/variables";

    .last-courses {
        a {
            border-bottom: 1px solid #696969;

            &:hover {
                border-color: $primary;
            }
        }
    }
</style>