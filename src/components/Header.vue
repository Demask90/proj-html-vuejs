<template>
  <header class="d-flex justify-content-between align-items-center">

    <a class="logoAgency" href="/"><img src="../assets/img/cropped-Group-39-2x.png" alt="Logo Phiox"></a>
    
    <nav class="d-flex">
      <a v-for="(link, index) in navLinks" :key="index" class="nav flex-nowrap" :href="link.url">{{link.text}}</a>
    </nav>

    <div id="SearchBuy" class="d-flex align-items-center">
      <BtnGradient msg="PURCHASE"/>
      <a class="IconSearch px-2" href="/"><i class="fas fa-search"></i></a>
    </div> 

  </header>
</template>

<script>
import Links from '@/assets/data/Links.js'
import Socials from '@/assets/data/Socials.js'
import BtnGradient from './BtnGradient.vue'
export default {
  name: 'Header',
  components: {
    BtnGradient,
  },
  data() {
    return {
      navLinks: Links.navLinks,
      socials: Socials.socials,
    }
  },
  methods: {

  }
}
</script>

<style scoped lang="scss">
@import '../styles/vars.scss';

header {
  width: 100%;
  height: 80px;
  position: sticky;
  top: 0;
  z-index: 1000;
  background-color: $headerBottom;
  
  .logoAgency {
    margin-left: 20px;

    img {
      width: 200px;
    }
  }

  .nav {
    padding: 0 20px;
    text-decoration: none;
    color: $Text;
  }

  #SearchBuy {
    margin-right: 20px;

    .IconSearch {
      color: $search;
    }
  }
}
</style>
