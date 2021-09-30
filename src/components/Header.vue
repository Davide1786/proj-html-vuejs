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
                qui vanno le icone del search hamburger e valiggia
              </div>
          </div>
          <div class="headerCenter">
              <h1>Contemporary Ideas</h1>
              <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.
                Eligendi quis natus totam veniam, commodi dolorum inventore,
                deleniti quasi laborum obcaecati blanditiis libero voluptatem error aut
                repudiandae facilis architecto ex? Blanditiis?</p>
              <div class="register">
                <div>Register Now</div>
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
    width: 100%;
    height: 100px;
    display: flex;
    justify-content: center;
    padding: 10px;
    top: 0%;
    left: 0%;
  }

  .logo {
    width: 20%;
    display: flex;
    align-items: center;
    padding: 20px;
  }

  .logo > img {
    width: 100%;
  }

  .navigazione {
    width: 60%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  ul, li {
    display: flex;
    list-style: none;
    margin: 20px;
    text-transform: uppercase;
    color: $bianco;
  }

  .icone {
    width: 20%;
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
  }

  .register {
    width: 180px;
    height: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: $azzurro;
    margin: 0px auto;
    text-transform: uppercase;
    color: $bianco;
  }
  
  .headerBottom {
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .cerchio {
    width: 20px;
    height: 20px;
    border: 2px solid $bianco;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 5px;
  }
 
  .pallino {
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background: $bianco;
  }

 
</style>
