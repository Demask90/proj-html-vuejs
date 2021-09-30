<template>
  <header>

    <div id="headerTop" class="d-flex justify-content-between align-items-center px-2">

      <div id="numberPhone">(001)88451234  88455438</div>

      <ul class="d-flex socials">
        <li v-for="(social, index) in socials" :key="index" class="socials">
          <a class="socialIcon" :href="social.url"><img :src="require(`../assets/img/${social.img}`)" :alt="socials.name"></a>
        </li>
      </ul>
     

    </div>

    <div id="headerBottom" class="d-flex justify-content-between align-items-center px-2">

      <a class="logoAgency" href="/"><img src="../assets/img/cropped-Group-39-2x.png" alt="Logo Phiox"></a>
      
      <nav class="d-flex">
        <a v-for="(link, index) in navLinks" :key="index" class="nav flex-nowrap" :href="link.url">{{link.text}}</a>
      </nav>

      <div id="SearchBuy" class="d-flex align-items-center">
        <b-button pill variant class="coloredBtn mx-2">PURCHASE</b-button>
        <a class="IconSearch" href="/"><i class="fas fa-search"></i></a>
      </div>

    </div>

  </header>
</template>

<script>
import Links from '@/assets/data/Links.js'
import Socials from '@/assets/data/Socials.js'

export default {
  name: 'Header',
  components: {
   
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

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../styles/vars.scss';
header {
  width: 100%;
  
  #headerTop {
    height: 30px;
    background-color: $headerTop;

    #numberPhone {
      color: $numberPhone;
      font-size: 0.8rem;
    }

    .socials {
      height: 30px;
      margin-block-start: 0;
      margin-block-end: 0;
      padding-inline-start: 0;
      list-style: none;

      .socialIcon {
        width: 100%;
        height: 30px;
        transition: 0.3s;
        
        img {
          width: 70%;
        }

        &:hover{
          filter: brightness(1.5);
        }
      }
    }
  }

  #headerBottom {
    height: 80px;
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

      .coloredBtn {
        background-image: $buyBtn;
        border: none;
        font-size: 0.6rem;
        padding: 10px 25px;
      }

      .IconSearch {
        color: $search;
      }
    }
  } 
}
</style>
