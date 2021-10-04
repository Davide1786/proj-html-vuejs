<template>
  <section>
    <div class="container">
      <div class="sfondo"></div>
      <div class="wrapperUno">
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
                <h3 class="professione"> {{img.professione}} </h3>
                <div :class="(img.status) ? 'active' : null" class="prezzo">
                  {{img.titolo}}
                </div>
                <!-- <div class="prezzo">ciao</div> -->
              </div>
              <p class="nome"> {{img.nome}} </p>
              <p class="articolo"> {{img.articolo}} </p>
              <p class="articolo"> Programming </p>
            </div>
            <!-- <div class="icone"></div> -->
          </div>
        </div>
        <div class="bottom">
          <div v-for="n in 3" :key="n" class="cerchio">
              {{n.cerchio}}
              <div class="pallino"></div>
          </div>
        </div>
        <div class="wrapperDue">
          <div class="topDue">
            <h1>Pricing Plans</h1>
            <p>Quaerat repellat libero molestiae obcaecati consequuntur laborum voluptatum, similique ipsum!</p>
          </div>
          <div class="centerDue">
            <div class="left">
              <div class="boxTop">
                <p class="save">Save up to 40% by paying weekly</p>
              </div>
              <div class="boxCella">
                <div v-for="(tab, index) in tabellasx" :key="index" class="cella">
                  <p class="titolo">{{tab.titolo}}</p>
                </div>
              </div>
            </div>
            <div class="right">
              <div class="boxsTop">
                <div v-for="(box, index) in boxAzzurri" :key="index" class="boxAzzurri">
                  <img :src="require(`../img/${box.img}`)" alt="">
                  <h3 class="piano"> {{box.piano}} </h3>
                  <p class="sottoColonna"> {{box.price}} </p>
                </div>
              </div>
              <div class="containerBox">
                <div class="boxContainer">
                  <div v-for="(tab, index) in colonnaSx" :key="index" class="righe">
                    <p class="testi"> {{tab.titolo}} </p>
                  </div>
                  <div class="righeSpecial">
                    <p class="testiSpecial">special</p>
                  </div>
                </div>
                <div class="boxContainer">
                  <div v-for="(tab, index) in colonnaCenter" :key="index" class="righe">
                    <p class="testi"> {{tab.titolo}} </p>
                  </div>
                  <div class="righeSpecial">
                    <p class="testiSpecial">special</p>
                  </div>
                </div>
                <div class="boxContainer">
                  <div v-for="(tab, index) in colonnaDx" :key="index" class="righe">
                    <p class="testi"> {{tab.titolo}} </p>
                  </div>
                  <div class="righeSpecial">
                    <p class="testiSpecial">special</p>
                  </div>
                </div>
              </div>
            </div>    
          </div>
        </div>
      </div>
    </div>
      <div class="containerLoghi">
        <div class="logotipi">
          <div v-for="(img, index) in loghi" :key="index" class="loghi">
            <img :src="require(`../img/${img.img}`)" alt="">
          </div>
        </div>
          
      </div>
    
  </section>
    
</template>

<script>
import immagini from '../data/immagini.js'
import boxAzzurri from '../data/boxAzzurri.js'
import tabellasx from '../data/tabellasx.js'
import colonnaSx from '../data/colonnaSx.js'
import colonnaCenter from '../data/colonnaCenter.js'
import colonnaDx from '../data/colonnaDx.js'
import loghi from '../data/loghi.js'

export default {
  name: 'MainBottom',
  data(){
    return {
      immagini: immagini,
      boxAzzurri: boxAzzurri,
      tabellasx: tabellasx,
      colonnaSx: colonnaSx,
      colonnaCenter: colonnaCenter,
      colonnaDx: colonnaDx,
      loghi: loghi
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../styles/variables';
@import '../styles/mixin';

.container {
  position: relative;
  width: 100%;
  height: 2300px;
  border-top: 1px solid grey;
  border-bottom: 1px solid grey;
  @include flex-column();
}

.sfondo {
  background-image: url('../img/page-background-img.png');
  @include wd100();
}

.wrapperUno {
  position: absolute;
  top: 0px;
  padding-top: 100px;
  @include wd100();
  @include column();
}

.top {
  width: 70%;
  margin: 50px auto;
  text-align: center;
}

h1 {
  margin-bottom: 20px;
  @include font60();
}

p {
  margin-bottom: 22px;
  @include font20();
}

.center {
  width: 95%;
  height: 500px;
  margin: 0px auto;
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

.professione {
  font-weight: bold;
  color: $titoliColonna;
}

.nome {
  margin-top: 5px;
  color: $nome;
  @include font15();
}

.articolo {
  color: $fontP;
  @include font18();
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
  margin: 30px auto;
  @include justify-content();
}

  .cerchio {
    margin: 0 5px;
    background: $azzurro;
    @include cerchio();
  }

  .wrapperDue {
  margin: 30px 0px;
  padding: 100px 0px;
  border-top: 1px solid grey;
  @include wd100();
  @include column();
}

.topDue {
  width: 70%;
  margin: 50px auto;
  text-align: center;
}

.centerDue {
  width: 95%;
  height: 100%;
  margin: 0 auto;
  display: flex;
}

.left {
  width: 30%;
}

.right {
  position: relative;
  width: 70%;
}

.boxTop {
  position: relative;
  width: 100%;
  height: 300px;
  border: 1px solid $griglia;
  border-top: 5px solid $borderTopColonna;
}

.save {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%);
  font-size: 30px;
  font-weight: bold;
  color: $titoliColonna;
  @include font25();

}

.piano {
  margin: 30px;
  font-weight: bold;
  color: $titoliColonna;
  @include font25();
}

.sottoColonna {
  font-weight: bold;
  color: $sottoTitoliColonna;
}

.boxCella {
  width: 100%;
  height: calc(100% - 300px);
}

.cella {
  position: relative;
  width: 100%;
  height: calc(100% / 8);
  border: 1px solid $griglia;
  color: $testiColonna;
  font-weight: bold;
}

.titolo {
  position: absolute;
  top: 50%;
  left: 25%;
  transform: translate(0%, -50%);
}

.boxsTop {
  width: 100%;
  height: 275px;
  display: flex;
  background: $backgroungGriglia;
}

.boxAzzurri {
  width: calc(100% / 3);
  height: 275px;
  border: 1px solid $griglia;
  border-top: 5px solid $borderTopColonna;
  @include column();
}

.containerBox {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: calc(100% - 275px);
  display: flex;
}

.boxContainer {
  width: calc(100% / 3);
  height: calc(100% - 50px);
}

.righe {
  width: calc(100%);
  height: calc(100% / 8);
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid $griglia;
  color: $testiColonna;
}

.testi {
  margin: 50% auto;
}

.righeSpecial {
  width: 100%;
  height: 90px;
  border: 1px solid $griglia;
  background: $backgroungGriglia;
  @include justify-content();
}

.testiSpecial {
  margin: 50% auto;
  width: 60%;
  height: 70%;
  border: 1px solid $griglia;
  text-transform: uppercase;
  color: $testiColonna;
  background: $bianco;
  @include justify-content();
}

.containerLoghi {
  width: 100%;
  height: 300px;
}

.logotipi {
  margin: 0 auto;
  width: 95%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.loghi {
  width: 100%;
  margin: 0 auto;
}

.loghi > img {
  width: 100%;
}


</style>
