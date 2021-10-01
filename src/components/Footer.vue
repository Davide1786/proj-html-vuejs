<template>
  <footer>
    <div class="backgroundFooter">
      <div class="link">
        <div class="academy">
          <img src="../img/logo-light.png" alt="">
          <ul>
            <li v-for="(link, index) in linksUno" :key="index">
              {{link.text}} <br> 
              {{link.textUno}} <br> 
              {{link.textDue}} <br> 
              {{link.textTre}} 
            </li>
          </ul>
        </div>
        <div class="popular">
          <h1>Popular courses</h1>
          <ul>
            <li v-for="(link, index) in linksDue" :key="index">
              {{link.text}} <br> {{ link.name}} 
            </li>
          </ul>
        </div>
        <div class="support">
          <h1>Support</h1>
          <ul>
            <li v-for="(link, index) in linksTre" :key="index">
              {{link.text}}
            </li>
          </ul>
        </div>
        <div class="learning">
          <h1>Flexible Learning</h1>
          <img src="../img/footer-img-1.png" alt="">
        </div>
      </div>
      <div class="footerBottom">
        <div class="copy">
          <p>Copyrights 2017 ©Mikado Themes</p>
        </div>
        <div class="socials">
          <p>CALL +44 300 303 0266</p>
          <p>FOLLOW US</p>
          <div class="icone"></div>
        </div>
      </div>
    </div>
  </footer>
    
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      linksUno: [
        {
          text: "Providing Life Changing",
          textUno: "Experiences Through",
          textDue: "Education Class That Fit your",
          textTre: "Busy life. closer to home",
          url: "#",
        },
        {
          text: "1-677-124-44227",
          url: "#",
        },
        {
          text: "mon - sat 8.00 - 18:00",
          url: "#",
        },
      ],
      linksDue: [
        {
          text: "Business english",
          name: "Preston marshall",
          url: "#",
        },
        {
          text: "social computing",
          name: "david sanders",
          url: "#",
        },
        {
          text: "learn spanish",
          name: "jennie king",
          url: "#",
        },
      ],
      linksTre: [
        {
          text: "User dashboard",
          url: "#",
        },
        {
          text: "Contact Us",
          url: "#",
        },
        {
          text: "FAQ",
          url: "#",
        },
        {
          text: "Course Offer",
          url: "#",
        },
        {
          text: "Events",
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


  .backgroundFooter {
    position: relative;
    width: 100%;
    height: 500px;
    background: $neroFooter;
    @include align-center();
  }

  .link {
    width: 95%;
    height: 300px;
    margin: 0 auto;
    @include display-flex();
    border-bottom: 1px solid $listFooter ;
  }

  .academy,
  .popular,
  .support,
  .learning {
    width: 20%;
    height: 100%;
    margin: 10px;
  }

  .academy > img {
    width: 150px;
    margin-bottom: 20px;
  }
  
  .learning > img {
    width: 100%;
  }

  h1 {
    margin-bottom: 20px;
    color: $bianco;
  }

  ul, li {
    list-style: none;
    margin-bottom: 20px;
    color: $listFooter;
  }

  .footerBottom {
    position: absolute;
    bottom: 0;
    left: 0;
    transform: translate(5.5%, -0%);
    width: 90%;
    margin: 0 auto;
    height: 100px;
    display: flex;
    color: $listFooter;
  }

  .copy {
    width: 50%;
    height: 100%;
    @include align-center();
  }

  .socials {
    width: 50%;
    height: 100%;
    @include align-center();
  }


</style>
