<template>
  <div id="app">
    <Header/>
    <Jumbotron/>
    <Films/>
    <BlueBanner/>
    <Footer/>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Jumbotron from '@/components/Jumbotron.vue'
import Films from '@/components/Films.vue'
import BlueBanner from '@/components/BlueBanner.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    Films,
    BlueBanner,
    Footer
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
@import '@/style/general.scss';
</style>
