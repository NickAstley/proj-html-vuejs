<template>
    <main>
        <!-- Div che serve per impostare lo sfondo con gradiente e la curva -->
        <div class="bg-gradient-curved">
            <!-- Sezione Work Culture -->
            <RowSection :section-name="`work-culture`"/>
            <!-- Sezione di display dei dati sui corsi -->
            <DataDisplay/>
            <!-- Sezione Upgrade Life -->
            <RowSection :section-name="`upgrade-life`"/>
            <!-- Sezione Latest Courses con generazione delle card -->
            <LatestCourses/>
        </div>
        <!-- Sezione People Hearts Us -->
        <RowSection :section-name="`people-hearts`"/>
        <!-- Sezione Transform You -->
        <RowSection :section-name="`transform-you`"/>
        <!-- Sezione OurBlogs -->
        <OurBlogs/>
        <!-- Sezione SubscribeNewsletters -->
        <SubscribeNewsletters/>
    </main>
</template>

<script>
    import RowSection from './main/RowSection';
    import DataDisplay from './main/DataDisplay';
    import LatestCourses from './main/LatestCourses';
    import OurBlogs from './main/OurBlogs';
    import SubscribeNewsletters from './main/SubscribeNewsletters';

    export default {
        components: {
            RowSection,
            DataDisplay,
            LatestCourses,
            OurBlogs,
            SubscribeNewsletters
        }
    }
</script>

<style lang="scss">
    @import "../assets/scss/variables";

    main {

        .bg-gradient-curved {
            background: linear-gradient(180deg, rgba(255,255,255,1) 0%, rgba(245,245,245,1) 100%);
            clip-path: ellipse(180% 100% at 50% 0%);
            margin-bottom: 5rem;
        }
    }
</style>