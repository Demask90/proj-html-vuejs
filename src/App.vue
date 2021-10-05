<template>
  <div id="app">
    <div class="container-fluid m-0 p-0">
      <bannerTop/>  
      <Header/>
      <Main/>
      <Footer/>
    </div>
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
