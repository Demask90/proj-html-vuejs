<template>
    <div class="d-flex lines">
        <div class="firstLine"></div>
        <div class="secondLine"></div>
    </div>
</template>

<script>
export default {
  name: 'lineGradient',
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

.lines {
    margin: 20px 0;
}
    .firstLine {
        height: 3px;
        border-radius: 30px;
        width: 8px;
        background-image: $footerGradientLine;
        margin-right: 4px;
    }

    .secondLine {
        height: 3px;
        width: 50px;
        border-radius: 30px;
        background-image: $footerGradientLine;    
    }
</style>
