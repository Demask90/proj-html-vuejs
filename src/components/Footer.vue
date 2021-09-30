<template>
  <footer>
    <div id="footerTop" class="d-flex ">

      <div id="agencyAbout" class="px-5" >
        <a class="logoAgency" href="/"><img class="pb-3" src="../assets/img/cropped-Group-39-2x.png" alt="Logo Phiox"></a>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos animi consequatur itaque numquam sint? Aliquam alias in fuga! Laborum magni odit dolorum repudiandae in iste minus expedita atque, ad quis.</p>
      </div>

      <div id="quickLinks" class="col-3 ">
        <h4>QUICK LINKS</h4>
        <ul>
          <li class="footerLink" v-for="(link, index) in footerLink" :key="index">
            <a :href="link.url">{{link.text}}</a>
          </li>
        </ul>
      </div>

      <div id="concact" class="col-3 px-5">
        <h4>CONTACT</h4>
        <div class="my-3">Patricia C. Amedee 4401 Waldeck street Gradivevine Nashville TX 76051</div>
        <div><a href="/">info@yourdomain.com</a></div>
        <div class="my-3">+99 (0) 101 0000 888</div>
      </div>

      <div id="locationMap" class="col-3 ">
        <h4>LOCATION ON MAP</h4>
        <img src="../assets/img/map.png" alt="location Map">
      </div>

    </div>



    <div id="footerBottom" class="d-flex justify-content-between align-items-center px-3">
      <div class="footerBottomText">
        <i class="far fa-copyright"></i> PHLOX BUSINESS THEME.
      </div>
      <ul class="d-flex socials">
        <li v-for="(social, index) in socials" :key="index" class="socials">
          <a class="socialIcon" :href="social.url"><img :src="require(`../assets/img/${social.img}`)" :alt="socials.name"></a>
        </li>
      </ul>
    </div>
  </footer>
</template>

<script>
import Links from '@/assets/data/Links.js'
import Socials from '@/assets/data/Socials.js'
export default {
  name: 'Footer',
  components: {
  },
  data() {
    return {
      footerLink: Links.footerLink,
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

footer {
  width: 100%;
  #footerTop {
    width: 100%;

    #agencyAbout {

      img {
        width: 200px;
      }
    }

    #quickLinks {
      ul {
        color: $Text;
        list-style: none;
        padding: 0;

        .footerLink { 
          a {
            color: $Text;
            padding: 0;
            text-decoration: none;
          }
        }
      }
    }

    #contact {
      div {
        font-size: 0.3rem;
      }
    }

    #locationMap {
      img {
        width: 87%;
      }
    }
  }

  #footerBottom {
    height: 80px;
    background-image: $footerBottom;

    .footerBottomText {
      color: $footerText;
    }

    .socials {
      margin-block-start: 0;
      margin-block-end: 0;
      padding-inline-start: 0;
      list-style: none;

      .socialIcon {
        width: 100%;
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
}

</style>
