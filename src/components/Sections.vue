<template>
<main>
  
  <section id="JumboSlider" class="d-flex align-items-center">

    <div id="jumboText" class="col-7">

      <div id="experiece">17 YEARS OF EXPERIENCE</div>
      <h1 id="title">We Are a <br> Web Design<span class="changeColor"> Agency</span></h1>
      <lineGradient class="my-5"/>
      <p id="agencyText">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quasi, et quidem dolore ipsa aliquam harum esse non numquam ab! Aspernatur doloremque eum iure consectetur animi aperiam quos, ex ipsam magnam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus neque repellat eum doloribus corporis. Natus aperiam in quo fuga sunt numquam eius dolor distinctio architecto. Quis odit officia qui ratione.</p>
      <b-button pill variant class="button my-4">READ MORE</b-button>
  
      <ul class="d-flex socialsName">
        <li v-for="(social, index) in socials" :key="index">
          <a :href="social.url">{{social.name}}</a>
        </li>
      </ul>
      <!-- predisporre slide jumbo -->
      <!-- set interval per scorrere le foto in automatico -->
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

  <section id="skills" class="d-flex align-items-center">
    <div class="textSkills col-5">
      <h2>We Are Here To Make Your <span class="changeColor">Website</span> Look More <span class="changeColor">Elegant</span> And Stylish!</h2>
      <lineGradient class="my-5"/>
      <b-button pill variant class="button">VIEW ALL</b-button>
    </div>
    <div class="boxSkills">
      <div v-for="(box, index) in skillsBox" :key="index" class="box float-start">
        <div class="boxIcon">{{box.icon}}</div>
        <div class="boxTitle">{{box.title}}</div>
        <div class="boxOverview">{{box.overview}}</div>
      </div>
    </div>
  </section>

  <section id="ourMission" class="d-flex align-items-center w-90">

    <div class="imgMission col-6">

      <img id="businessWoman" src="@/assets/img/businesswoman-analysing-document-P8WSNMC-1024x820.jpg" alt="businesswoman analysing document">
      
      <div id="ArchitectObs">
        <div id="Architect">
          <img src="@/assets/img/busy-architect-PYVKWM4-1024x872.jpg" alt="Busy Architect">
          <div class="overlay"></div> 
        </div>
      </div>
      
    </div>

    <div class="textMission col-6">

      <h2>learn more about our <span class="colorChange">missions</span></h2>
      <lineGradient class="my-5"/>
      <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Autem quibusdam voluptatibus pariatur natus nobis libero, ad cum porro maxime temporibus harum vel sit, dolorum vitae dolores nesciunt facere quo sed.</p>
      <b-button pill variant class="button my-4">READ MORE</b-button>
    
    </div>

  </section>
  <section></section>
  <section></section>
  <section></section>
  <section></section>

</main>
 
</template>

<script>
import lineGradient from '../components/lineGradient.vue'
import Socials from '@/assets/data/Socials.js'
import SkillsBox from '@/assets/data/SkillsBox.js'
export default {
  name: 'Sections',
  components: {
    lineGradient,
  },
  data() {
    return {
      socials: Socials.socials,
      skillsBox: SkillsBox.skillsBox
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
  margin-bottom: 150px;
  background-color: $backgroundJumbo;

  #jumboText {
    max-height: 100vh;
    position: relative;
    padding: 100px 0 100px 150px;

    #experiece {
      color: $search;
      letter-spacing: 15px;
    }

    #title {
      font-weight: 700;
      font-size: 5rem;
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
      left: 86%;
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

#skills {
  width: 90%;
  margin: 0 auto;

  .textSkills {
    padding: 20px 20px 20px 0;
    h2 {
      font-weight: bold;
      font-size: 2.5rem;
      
    }

    @include button('BtnGreen');
    
  }
  .boxSkills {
    
    .box {
      width: calc(50% - 40px);
      padding: 20px;
      margin: 20px;
      border-radius: 20px;
      box-shadow: 0px 0px 15px 0px $shadowButtonDark;

      .boxIcon {
        padding: 30px 10px;

      }

      .boxTitle {
        font-weight: bold;
        padding: 10px 0;
      }

      .boxOverview {  
        font-size: 0.8rem;
      }
    }
  }

}

#ourMission {
  margin: 150px 0;
  padding: 150px 0;
  background-color: $backgroundMission;
  z-index: -2;

  .imgMission {
    text-align: center;
    padding: 50px;
    position: relative;
    

    #businessWoman{
      position: absolute;
      top: 60%;
      left: 60%;
      width: 60%;
      transform: translate(-50%, -50%);
      z-index: 10;
      border-radius: 10px;
      box-shadow:0px 0px 15px 0px $shadowButtonDark;
    }

    #ArchitectObs {
      position: absolute;
      top: 20%;
      left: 65%;
      width: 95%;
      transform: translate(-50%, -50%);
      
      #Architect{
        position: relative;
        width: 60%;
        z-index: 9;
        border-radius: 10px;
        box-shadow:0px 0px 15px 0px $shadowButtonDark;
       

        img {
          width: 100%;
          border-radius: 10px;
        }

        .overlay {
          position: absolute; 
          width: 100%; 
          height: 100%; 
          top: 0;
          left: 0;
          right: 0;
          bottom: 0;
          background-image: $buyBtn;
          opacity: 0.8;
          border-radius: 10px;
          z-index: 2; 
          cursor: pointer; 
        }
      }
    }
  }
  .textMission {
    padding: 50px;

    h2 {
      font-weight: bold;
      font-size: 2.5rem;
      
    }

    @include button('BtnGreen');
  }
}
</style>
