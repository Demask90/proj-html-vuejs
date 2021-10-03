<template>
<main>
  
  <section id="jumboSlider" class="d-flex align-items-center">

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

  <section id="ourMission" class="d-flex align-items-center">

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

  <section id="caseHistory" class="d-flex flex-column">

    <div id="caseHistoryText" class="d-flex row align-items-center">

      <h2 class="col-6 p-3">
        <lineGradient class="my-5"/>
        Our recent <span class="changeColor">web design </span>& some example of past <span class="changeColor">projects</span> 
        <lineGradient class="my-5"/>
      </h2>

      <p class="col-6 p-3 ">
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Similique animi, impedit repellat, id amet nam ad dolorum repudiandae itaque iure facere? Quod necessitatibus ex saepe et. Repudiandae eveniet perspiciatis ullam. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Neque omnis, autem dignissimos accusamus dolor eaque, explicabo, nemo ut nihil quaerat assumenda labore provident libero! Nobis libero nisi optio pariatur repudiandae.
      </p>

    </div>

    <ul id="caseHistoryImg" >
      <li class="boxImg form-check-inline" v-for="(caseHistory, index) in caseHistory" :key="index"> 
          <img :src="require(`../assets/img/${caseHistory.img}`)" alt="caseHistory.text">
      </li>
    </ul>

    <b-button pill variant class="button align-self-center">READ MORE</b-button>
  </section>

  <section id="feedback">

    <div class="overlayDark d-flex flex-column align-items-center justify-content-center">

      <i class="fas fa-quote-left changeColor"></i>

      <h4 class="col-8">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Reprehenderit excepturi voluptatem fuga sint molestiae voluptatibus veniam quia quas repellat, provident sequi illum aliquam dolore natus cupiditate! Repudiandae tempora mollitia deleniti.</h4>
        
      <img src="@/assets/img/businesswoman-analysing-document-P8WSNMC-1024x820.jpg" alt="businesswoman analysing document">

      <h5 class="changeColor">LISSA DURBLIN</h5>

      <div class="status">Client</div>

    </div>

    
  </section>

  <section id="blogNews" class="d-flex flex-column align-items-center">

    <h2>Latest News & Our <span class="changeColor">Blog</span></h2>

    <lineGradient class="my-5"/>

    <ul id="newsBoxs" class="d-flex flex-row">
      <li class="boxNews form-check-inline" v-for="(news, index) in newsBlog" :key="index">

        <img :src="require(`../assets/img/${news.img}`)" alt="news.text">

        <div class="boxInfoNews"> 
          <div class="dateColor">{{news.date}} <span>by -</span> {{news.author}}</div>
          <i class="fas fa-circle"></i><span class="boxNewsTitle">{{news.title}}</span>
        </div>
        
      </li>
    </ul>
    
    <b-button pill variant class="button align-self-center">VIEW ALL POST</b-button>

  </section>

  <section id="startAboutPartners"> 
    <div id="startAbout" class="d-flex justify-content-center">

      <div class="start box d-flex flex-column align-items-center">
        <div class="TopHint">Are You Ready?</div>
        <h3>Start a New Project</h3>

        <div class="submitStart">
          <input class="inputStart" type="text" name="mail" placeholder="Enter Your Email Address">
          <button class="btnStart" id="buttonMail">SUBMIT</button>
        </div>
      </div>

      <div class="about box d-flex flex-column align-items-center">
        <div class="TopHint">What Are You Waiting For?</div>
        <h3>Let's Talk About Work</h3>
        <b-button pill variant class="button align-self-center">VIEW ALL POST</b-button>
      </div>

    </div>
    
    <ul id="partners" class="d-flex justify-content-around">
      <li class="boxPartner form-check-inline p-0 m-0" v-for="(partner, index) in partners" :key="index"> 
          <img :src="require(`../assets/img/${partner.logo}`)" alt="partner.text">
      </li>
    </ul>

  </section>

</main>
 
</template>

<script>
import lineGradient from '../components/lineGradient.vue'
import Socials from '@/assets/data/Socials.js'
import SkillsBox from '@/assets/data/SkillsBox.js'
import CaseHistory from '@/assets/data/CaseHistory.js'
import NewsBlog from '@/assets/data/NewsBlog.js'
import Partners from '@/assets/data/Partners.js'
export default {
  name: 'Sections',
  components: {
    lineGradient,
  },
  data() {
    return {
      socials: Socials.socials,
      skillsBox: SkillsBox.skillsBox,
      caseHistory: CaseHistory.caseHistory,
      newsBlog: NewsBlog.newsBlog,
      partners: Partners.partners,
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

#jumboSlider {
  width: 100%;
  height: 100vh;
  position: relative;
  margin-bottom: 150px;
  background-color: $backgroundJumbo;

  #jumboText {
    max-height: 100vh;
    position: relative;
    padding: 100px 0 100px 100px;

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
  width: 100%;
  height: 100vh;
  margin: 150px 0;
  padding: 150px 0;
  background-color: $backgroundMission;
  z-index: -2;

  .imgMission {
    height: 100%;
    text-align: center;
    position: relative;
    

    #businessWoman{
      position: absolute;
      top: 50%;
      left: 55%;
      width: 60%;
      transform: translate(-50%, -50%);
      z-index: 10;
      border-radius: 10px;
      box-shadow:0px 0px 15px 0px $shadowButtonDark;
    }

    #ArchitectObs {
      position: absolute;
      top: 40%;
      left: 60%;
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

#caseHistory {
  width: 90%;
  margin: 0 auto;
  #caseHistoryText{
    h2 {
      font-size: 2.5rem;
      font-weight: bold;
    }
  }
  #caseHistoryImg{
  padding: 0;
    .boxImg {
      width: calc(25% - 10px);
      margin: 1px 5px;


      img {
        width: 100%;
        border-radius: 10px;
      }
    }
  }
  @include button('BtnGreen');
  button {
    margin: 100px 0;
    }
    
}

#feedback {
  background-image: url("../assets/img/four-businesspeople-in-a-boardroom-with-paperwork-PC4V8H4.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  height: 100vh;
  opacity: 0.8;
  margin: 100px 0 200px 0;

  .overlayDark {
    background-image: $feedbackBackground;
    width: 100%;
    height: 100%;
    
    .fa-quote-left{
    font-size: 3rem;
    margin:40px 0;
    }

    h4{
      color: $SocialIcon;
      line-height: 50px;
    }

    img {
      width: 120px;
      height: 120px;
      margin: 40px 0 20px 0;
      border-radius: 50%;
      border: 2px solid $SocialIcon;
    }

    .status {
      color: $SocialIcon;
    }
  } 
}

#blogNews {
  width: 100%;
  margin: 100px 0 50px 0;
  #newsBoxs {
    width: 90%;
    margin: 0 auto;
    list-style: none;
    margin-block-start: 0;
    margin-block-end: 0;
    padding-inline-start: 0;

     .boxNews {
        position: relative;
        width: calc(100% / 3);

        img {
          width: 100%;
          border-radius: 10px;
          box-shadow:0px 0px 15px 0px $shadowButtonDark;
        }

        .boxInfoNews {
          position: absolute;
          width: 80%;
          margin: 0 auto;
          background-color: white;
          box-shadow:0px 0px 15px 0px $shadowButtonDark;
          border-radius: 5px;
          padding: 20px 30px;
          top: 100%;
          left: 50%;
          transform: translate(-50%, -50%);

          .dateColor {
            color: grey;
            font-size: 0.7rem;
          }

          .fa-circle {
            color: $search;
            padding-right: 5px;
            font-size: 0.7rem;
          }
          .boxNewsTitle {
            font-weight: bold;
            font-size: 1.1rem;
          }
        }
    }
  }
  @include button('BtnDark');
  button {
    margin: 150px 0;
  }
 
}

#startAboutPartners {
  width: 100%;
  margin: 40px auto;
  
  #startAbout{
    color: white;

    .box {
      width: calc(100% - 20px);
      padding: 50px 140px;
      border-radius: 10px;
      margin: 0 10px;

      .TopHint {
        font-size: 0.9rem;
        padding: 10px;
      }

      h3{
        padding-bottom: 30px;
        font-weight: bold;
      }
    }
    .start{
      background-image: $footerBottom;
      box-shadow:0px 0px 15px 0px $shadowButtonDark;

      .submitStart {
        width: 100%;
        text-align: center;

        .inputStart {
          background-color: $Text;
          padding: 15px;
          border-radius: 50px 0 0 50px;
          border: none;
          color: lightgray;
          font-size: 0.8rem;
        }

        .btnStart {
          background-color: $Text;
          padding: 15px;
          border-radius: 0 50px 50px 0;
          border: none;
          color: lightgray;
          font-size: 0.8rem;
        }
      }
    }
    .about{
      background-image: $activeBackground;
      box-shadow:0px 0px 15px 0px $shadowButton;
      @include button('BtnDark');
    }
  }
  #partners {
    background-color: $backgroundPartners;
    // box-shadow:0px 0px 15px 0px $shadowButtonDark;
    padding: 100px 0 150px;
  }
}
</style>
