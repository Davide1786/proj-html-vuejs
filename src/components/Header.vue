<template>
  <header>
      <div class="backgroundHeader">
         <div class="scuro"></div>
          <div class="headerTop">
              <div class="logo">
                  <img src="../img/logo-light.png" alt="">
              </div>
              <nav class="navigazione">
                  <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a> {{link.text}} </a>
                    </li>
                  </ul>
              </nav>
              <div class="icone">
                <i class="fas fa-search"></i>
                <i class="far fa-clipboard"><div class="qnt"> 0 </div></i>
                <!-- <div class="qnt">0</div> -->
                <i class="fas fa-bars"></i>
              </div>
          </div>
          <div class="headerCenter">
              <h1>Contemporary Ideas</h1>
              <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.
                Eligendi quis natus totam veniam, commodi dolorum inventore,
                deleniti quasi laborum obcaecati blanditiis libero voluptatem error aut
                repudiandae facilis architecto ex? Blanditiis?</p>
              <div class="register">
                <!-- <div> -->
                  <p class="now">Register Now</p>
                <!-- </div> -->
              </div>
          </div>
          <div class="headerBottom">
              <div v-for="n in 3" :key="n" class="cerchio">
                  {{n.cerchio}}
                  <div class="pallino"></div>
              </div>
          </div>
      </div>
  </header>   
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      links: [
        {
          text: "Home",
          url: "#",
        },
        {
          text: "Courses",
          url: "#",
        },
        {
          text: "Istructor",
          url: "#",
        },
        {
          text: "Events",
          url: "#",
        },
        {
          text: "Pages",
          url: "#",
        },
        {
          text: "Elements",
          url: "#",
        },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

@import '../styles/variables';
@import '../styles/mixin';

  .backgroundHeader {
    position: relative;
    width: 100%;
    height: 900px;
    background-image: url('../img/course-9-f-img.jpg');
    background-repeat: no-repeat;
    background-size: cover;
  }

  .scuro {
    position: absolute;
    width: 100%;
    height: 100%;
    background: rgb(6, 6, 6, 0.2);
  }

  .headerTop {
    position: absolute;
    left: 50%;
    transform: translate(-50%);
    width: 95%;
    height: 100px;
    margin: 0px auto;
    @include display-flex();
    @include w-90();
  }

  .logo {
    text-align: start;
    width: 200px;
    @include align-center();
  }

  .logo > img {
    width: 100%;
  }

  // .navigazione {
  //   width: calc(100% - 400px);
  //   @include justify-content();
  // }

  ul, li {
    width: 100%;
    display: flex;
    list-style: none;
    margin: 20px;
    text-transform: uppercase;
    color: $bianco;
  }

  .icone {
    text-align: end;
    width: 200px;
  }

  .fas {
    margin-right: 20px;
    font-size: 20px;
    color: $bianco;
  }

  .qnt {
  position: absolute;
  top: 0;
  right: 0;
  transform: translate(60%, -20%);
  width: 15px;
  height: 15px;
  border-radius: 50%;
  background: $azzurro;
  font-size: 12px;
  @include justify-content();
}

.fa-clipboard {
  position: relative;
  margin-right: 20px;
    font-size: 20px;
    color: $bianco;
}

 .headerCenter {
    position: absolute;
    width: 80%;
    margin: 0 auto;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
  }

  h1 {
    font-size: 90px;
    margin-bottom: 30px;
    color: $bianco;
  }

  p {
    margin-bottom: 30px;
    color: $bianco;
    @include font20();
  }

  .register {
    position: relative;
    width: 200px;
    height: 70px;
    margin: 0px auto;
    text-transform: uppercase;
    background: $azzurro;
    color: $bianco;
  }

  .now {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 80%;
    @include font18();
  }
  
  .headerBottom {
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 50px;
    @include justify-content();
  }

  .cerchio {
    width: 20px;
    height: 20px;
    margin: 0 5px;
    border-radius: 50%;
    border: 2px solid $bianco;
    @include justify-content();
  }
 
  .pallino {
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background: $bianco;
  }

 
</style>
