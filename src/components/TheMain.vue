<template>
    <main>
        <div class="container">
            <!-- Sezione Work Culture -->
            <WorkCulture/>
            <UpgradeLife/>
        </div>
    </main>
</template>

<script>
    import WorkCulture from './main/WorkCulture';
    import UpgradeLife from './main/UpgradeLife';

    export default {
        components: {
            WorkCulture,
            UpgradeLife
        }
    }
</script>

<style lang="scss">
    main {
        padding-top: 5rem;
        padding-bottom: 5rem;

        section {
            padding-top: 5rem;
            padding-bottom: 5rem;
        }
    }
</style>