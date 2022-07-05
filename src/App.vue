<template>
  <div id="app">
    <TheHeader/>
    <TheMain/>
    <TheFooter/>
  </div>
</template>

<script>
  import TheHeader from './components/TheHeader'
  import TheMain from './components/TheMain'
  import TheFooter from './components/TheFooter'

  export default {
    name: 'App',
    components: {
      TheHeader,
      TheMain,
      TheFooter
    }
  }
</script>