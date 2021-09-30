<template>
<main>
  
  <section id="JumboSlider" class="d-flex align-items-center">
    <div id="jumboText" class="col-6">
      <div >17 YEARS OF EXPERIENCE</div>
      <h1>We Are a Web Design<span>Agency</span></h1>
      <lineGradient/>
      <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quasi, et quidem dolore ipsa aliquam harum esse non numquam ab! Aspernatur doloremque eum iure consectetur animi aperiam quos, ex ipsam magnam.</p>
    </div>
    <div id="jumboImg" class="col-6">

    </div>
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
export default {
  name: 'Sections',
  components: {
    lineGradient
  },
  data() {
    return {

    }
  },
  methods: {

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../styles/vars.scss';
  #JumboSlider {
    width: 100%;
    #jumboImg {
      width: 60%;
      height: 100vh;
      background-image: url("../assets/img/Group-36-2x.png");
      background-repeat: no-repeat;
      background-size: cover;
      background-position: center;
    }
  }
</style>
