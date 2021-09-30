<template>
    <div id="headerTop">

        <div id="numberPhone">(001)88451234  88455438</div>

        <div class="socials">
            <ul class="d-flex">
                <li v-for="(social, index) in socials" :key="index">
                <a class="socialIcon" :href="social.url"><img :src="require(`../assets/img/${social.img}`)" :alt="socials.name"></a>
                </li>
            </ul>
        </div>

    </div>
</template>

<script>
import Socials from '@/assets/data/Socials.js'
export default {
  name: 'Header',
  components: {
  },
  data() {
    return {
      socials: Socials.socials,
    }
  },
  methods: {

  }
}
</script>

<style scoped lang="scss">
@import '../styles/vars.scss';
 #headerTop {
    background-color: $headerTop;
    height: 30px;

    #numberPhone { 
      float: left;
      height: 30px;
      line-height: 30px;
      color: $numberPhone;
      font-size: 0.8rem;
      padding-left: 5px;
    }

    .socials {
      float: right;
      height: 30px;
      margin-block-start: 0;
      margin-block-end: 0;
      padding-inline-start: 0;


      ul{
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
  }
</style>