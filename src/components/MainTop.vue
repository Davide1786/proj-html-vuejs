<template>
  <section>
    <div class="subjects">
      <div class="containerIcons">
        <div v-for="(icon, index) in icons" :key="index" class="icons">
          <img :src="require(`../img/${icon.img}`)" alt="">
          <h3> {{icon.text}} </h3>
        </div>
      </div>
    </div>
    <div class="testo">
      <h1>The Trusted Name <br> for In-Home Tutoring.</h1>
      <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officiis autem, eveniet omnis fugiat alias excepturi, magni doloremque similique fuga quae rerum minus voluptatibus, et minima tempore laudantium optio temporibus voluptas?</p>
      <p class="more">Learn MORE</p>
    </div>
    <div class="jumbotron">
      <img src="../img/h5-img-1.jpg" alt="">
    </div>
    <div class="mondo">
      <div class="mappamondo">
        <img src="../img/h5-img-2.jpg" alt="">  
      </div>
      <div class="textEmpowering">
        <h1 class="empowering">
          Empowering <br> Children to Reach <br> Their Potential
        </h1>
        <p class="lorem">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quos accusamus, alias rerum expedita commodi illum consequuntur? Sapiente consectetur vitae repellendus facere dolorem mollitia suscipit quae ducimus, quasi ab veritatis officia!</p>
        <div class="number">
          <div>
            <p class="user">168</p>
            <p class="userText"> User Stories</p>
          </div>
          <div>
            <p class="event">347</p>
            <p class="eventText">Events</p>
          </div>
        </div>
      </div>
    </div>
  </section>
    
</template>

<script>
import icons from '../data/icons.js'
export default {
  name: 'MainTop',
  data() {
    return {
      icons : icons
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../styles/variables';
@import '../styles/mixin';

.subjects {
  width: 100%;
  height: 300px;
  margin-top: 50px;
}

.containerIcons {
  width: 95%;
  height: 300px;
  margin: 0 auto;
  @include display-flex();
}

.icons {
  width: calc(1200px / 6);
  margin: 3px;
  // width: calc(95% / 6);
  height: 250px;
  background: $backgroungIcons;
  @include column();
}

h3 {
  margin-top: 15px;
}

h1 {
  @include font50();
}

.testo {
  width: 95%;
  margin: 50px auto;
}

p {
  margin-top: 25px;
  color: $fontP;
  @include font22();
}

.more {
  width: 95%;
  margin-top: 25px;
  text-transform: uppercase;
  color: $azzurro;
  @include font18();
}

.jumbotron {
  width: 95%;
  text-align: center;
  margin: 0 auto;
}

.jumbotron > img {
  width: 100%;
}

.mondo {
  width: 95%;
  margin: 50px auto;
  @include justify-center();
}

.mappamondo {
  width: 50%;
  display: flex;
  align-items: flex-end;
  justify-content: center;
}

.mappamondo > img {
  width: 100%;
}

.textEmpowering {
  width: 50%;
  padding: 30px;
}

.empowering {
  @include font50();
}

.lorem {
  margin: 40px auto;
}

.number {
  display: flex;
}

.user, .event {
  font-size: 60px;
  font-weight: bold;
  color: $azzurro;
}

.userText, .eventText {
  margin-top: 0px;
  color: $azzurro;
}

.user {
  margin-right: 150px;
}


</style>
