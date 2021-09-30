<template>
     <b-button pill variant class="coloredBtn mx-2">{{msg}}</b-button>
</template>

<script>
export default {
  name: 'BtnGradient',
    props: {
    msg: String
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
.coloredBtn {
        background-image: $buyBtn;
        box-shadow: 0px 0px 15px 0px $shadowButton;
        border: none;
        font-size: 0.7rem;
        padding: 12px 25px;
      }
    
</style>
