<template>
  <div id="app">
    <bannerTop/>  
    <Header/>
    <Main/>
    <Footer/>
  </div>
</template>

<script>
import bannerTop from './components/bannerTop.vue';
import Header from './components/Header.vue';
import Main from './components/Sections.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    bannerTop,
    Header,
    Main,    
    Footer,
  }
}
</script>,

<style lang="scss">
@import "./styles/generals.scss";

</style>
