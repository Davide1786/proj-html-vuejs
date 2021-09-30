<template>
  <footer>
    <div class="backgroundFooter">
      <div class="link">
        <div class="academy"></div>
        <div class="popular"></div>
        <div class="support"></div>
        <div class="learning"></div>

      </div>

    </div>
  </footer>
    
</template>

<script>
export default {
  name: 'Footer',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

@import '../styles/variables';

  .backgroundFooter {
    width: 100%;
    height: 500px;
    background: $neroFooter;
    display: flex;
    align-items: center;
  }

  .link {
    width: 90%;
    height: 400px;
    display: flex;
    justify-content: center;
    align-items: center;
    background: blueviolet;
  }

  .academy,
  .popular,
  .support,
  .learning {
    width: 20%;
    height: 100%;
    background: chartreuse;
    margin: 10px;
    margin: 20px;
  }
</style>
