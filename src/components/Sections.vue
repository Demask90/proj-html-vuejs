<template>
<main>
  
  <section id="JumboSlider" class="d-flex align-items-center">

    <div id="jumboText" class="col-7">
      <div id="experiece">17 YEARS OF EXPERIENCE</div>
      <h1 id="title">We Are a <br> Web Design<span id="agencyColor"> Agency</span></h1>
      <lineGradient class="my-5"/>
      <p id="agencyText">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quasi, et quidem dolore ipsa aliquam harum esse non numquam ab! Aspernatur doloremque eum iure consectetur animi aperiam quos, ex ipsam magnam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus neque repellat eum doloribus corporis. Natus aperiam in quo fuga sunt numquam eius dolor distinctio architecto. Quis odit officia qui ratione.</p>
      <b-button pill variant class="button my-4">READ MORE</b-button>
      <ul class="d-flex socialsName">
        <li v-for="(social, index) in socials" :key="index">
          <a :href="social.url">{{social.name}}</a>
        </li>
      </ul>
      <div id="sliderImg">
      <ul class="d-flex align-items-center slider">
        <li class="counter active">01</li>
        <li class="counter">02</li>
        <li class="counter">03</li>
      </ul>
    </div>
    </div>
    <div id="jumboImg"></div>
    
  </section>

  <section></section>
  <section></section>
  <section></section>
  <section></section>
  <section></section>
  <section></section>

</main>
 
</template>

<script>
import lineGradient from '../components/lineGradient.vue'
import Socials from '@/assets/data/Socials.js'
export default {
  name: 'Sections',
  components: {
    lineGradient
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

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../styles/vars.scss';
@import "../styles/mixins";
  #JumboSlider {
    width: 100%;
    height: 100vh;
    position: relative;

    #jumboText {
      position: relative;
      padding: 100px 0 100px 150px;

      #experiece {
        color: $search;
        letter-spacing: 15px;
      }

      #title {
        font-weight: 700;
        font-size: 5rem;

        #agencyColor {
          color: $search;
        }
      }

      @include button('BtnDark');

      .socialsName {
        padding: 30px 0 0 0;
        list-style: none;
        li {
          a{
            color: black;
            padding-right: 20px;
            text-decoration: none;
            text-transform: uppercase;
            font-weight: bold;
          }
        }
      }

      #sliderImg {
        list-style: none;
        position: absolute;
        top: 83%;
        left: 85%;
        transform: translate(-50%, -50%);
        background-image: $sliderBackground;
        padding: 2px;
        border-radius: 20px;

        .slider {
          list-style: none;
          margin: 0;
          padding: 0;

          .counter {
            color: $numberPhone;
            padding: 6px 12px;
          }
          .active {
            padding: 6px 13px;
            border-radius: 20px;
            background-image: $activeBackground;
            color: $SocialIcon;
          }
        }
      }
    }

    #jumboImg {
      width: 60%;
      height: 100vh;
      background-image: url("../assets/img/Group-36-2x.png");
      background-repeat: no-repeat;
      background-size: cover;
      background-position: center;
      position: absolute;
      top: 50%;
      left: 80%;
      transform: translate(-50%, -50%);
    }
  }
</style>
