<template>
    <main>
        <div class="bg-gradient-curved">
            <div class="container">
                <!-- Sezione Work Culture -->
                <WorkCulture/>
                <!-- Sezione Work Culture -->
                <UpgradeLife/>
                <!-- Sezione Latest Courses con generazione delle card -->
                <LatestCourses/>
            </div>
        </div>
    </main>
</template>

<script>
    import WorkCulture from './main/WorkCulture';
    import UpgradeLife from './main/UpgradeLife';
    import LatestCourses from './main/LatestCourses';

    export default {
        components: {
            WorkCulture,
            UpgradeLife,
            LatestCourses
        }
    }
</script>

<style lang="scss">
    main {
        padding-top: 5rem;
        padding-bottom: 5rem;

        .bg-gradient-curved {
            background: linear-gradient(180deg, rgba(255,255,255,1) 0%, rgba(245,245,245,1) 100%);
            clip-path: ellipse(180% 100% at 50% 0%);
        }
        section {
            padding-top: 5rem;
            padding-bottom: 5rem;
        }
    }
</style>