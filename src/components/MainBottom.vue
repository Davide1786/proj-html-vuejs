<template>
  <section>
    <div class="wrapperUno">
      <div class="sfondo"></div>
      <div class="container">
        <div class="top">
          <h1>Popular Online Courses</h1>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat repellat libero molestiae obcaecati consequuntur laborum voluptatum, similique ipsum! Rerum ut facilis quis mollitia quasi facere illum dignissimos saepe dolorum fuga?</p>
        </div>
        <div class="center">
          <div v-for="(img, index) in immagini" :key="index" class="box">
            <div class="box-img">
                <img :src="require(`../img/${img.img}`)" alt="">
            </div>
            <div class="box-description">
              <div class="fasciaPrezzo">
                <h3> {{img.professione}} </h3>
                <div :class="(img.status) ? 'active' : null" class="prezzo">
                  {{img.titolo}}
                </div>
                <!-- <div class="prezzo">ciao</div> -->
              </div>
              <p class="nome"> {{img.nome}} </p>
              <p class="articolo"> {{img.articolo}} </p>
              <p class="articolo"> sostituire </p>
            </div>
            <div class="icone"></div>
          </div>
        </div>
        <div class="bottom">
          <div v-for="n in 3" :key="n" class="cerchio">
                  {{n.cerchio}}
                  <div class="pallino"></div>
              </div>
        </div>
      </div>
    </div>
  </section>
    
</template>

<script>
import immagini from '../data/immagini.js'
export default {
  name: 'MainBottom',
  data(){
    return {
      immagini: immagini,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../styles/variables';
@import '../styles/mixin';

.wrapperUno {
  position: relative;
  width: 100%;
  height: 1000px;
  border-top: 1px solid grey;
  border-bottom: 1px solid grey;
  padding: 10px;
  @include flex-column();
}

.sfondo {
  background-image: url('../img/page-background-img.png');
  
  background-size: 190%;
  background-position: 0px -15px;
  transform: rotate(-180deg);
  // background-repeat: no-repeat;
  // background-size: 190%;
  // background-position: 0px -15px;
  // transform: rotate(-180deg);
  @include wd100();
}

.container {
  position: absolute;
  @include wd100();
  @include column();
}

.top {
  width: 70%;
  margin: 50px auto;
  text-align: center
}

h1 {
  margin-bottom: 20px;
  @include font60();
}

p {
  margin-bottom: 22px;
  @include font20();
}

.articolo {
  @include font18();
}

.nome {
  margin-top: 5px;
  @include font15();
}

.center {
  width: 95%;
  height: 500px;
  margin: 0 auto;
  @include align-center();
}

.box {
  width: calc(100% / 3);
  height: 450px;
  margin: 0px 5px;
}

.box-img {
  width: 100%;
  height: 200px;
}

.box-img > img {
  object-fit: cover;
  @include wd100();
}

.box-description {
  padding: 15px;
  height: 250px;
  border: 1px solid rgb(206, 206, 206);
  overflow: scroll;
}

.fasciaPrezzo {
  @include space-between(); 
     .active {
          height: 100%;
          background: $backgroungPrice;
        }
}

.prezzo {
  width: 50px;
  height: 100%;
  border-radius: 20px;
  padding: 2px;
  background: $azzurro;
  color: $bianco;
  text-transform: uppercase;
  @include justify-content();
  @include font13();
}

.bottom {
  width: 50%;
  height: 30px;
  margin: 0 auto;
  @include justify-content();
}

  .cerchio {
    margin: 0 5px;
    background: $azzurro;
    @include cerchio();
  }
</style>
