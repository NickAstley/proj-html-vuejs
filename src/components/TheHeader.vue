<template>
    <header>
        <TheNavbar/>
        <TheJumbotron/>
    </header>
</template>

<script>
    import TheNavbar from './header/TheNavbar';
    import TheJumbotron from './header/TheJumbotron';

    export default {
        components: {
            TheNavbar,
            TheJumbotron
        }
    }
</script>