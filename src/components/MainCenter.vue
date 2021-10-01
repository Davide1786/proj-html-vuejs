<template>
  <section>
    <div class="jumbotron">
      <div class="utente">
        <img src="../img/testimonials-standard-2.png" alt="">
      </div>
      <div class="testo">
        <p>"Lorem ipsum dolor sit amet consectetur adipisicing elit. Excepturi, eum praesentium aliquam molestias voluptas deleniti, suscipit, maxime quo nostrum natus rem cum voluptatum repellat eligendi vero cumque. Harum, inventore ex! aliquam molestias voluptas deleniti"</p>
      </div>
      <div class="nome">Joan Collins</div>
      <div class="studente">STUDENT</div>
      <div class="headerBottom">
              <div v-for="n in 3" :key="n" class="cerchio">
                  {{n.cerchio}}
                  <div class="pallino"></div>
              </div>
          </div>
    </div>
    <div class="info">
      <div class="celle">
        <div v-for="(riga, index) in righe" :key="index" class="righe">
          <div :class="(riga.status) ? 'active, test' : null"></div>
            <p class="barra">{{riga.titolo}}</p>   
        </div>
      </div>
      <div class="articolo">
        <div class="titolo">
          <h1 class="learning">Learning Possibilities</h1>
          <p class="lorem">Lorem ipsum dolor sit amet consectetur adipisicing elit. Ex accusamus excepturi consequatur vel, amet optio temporibus nobis reiciendis? Laudantium quaerat tempora, id natus quasi possimus esse rem molestias ullam minima.
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Autem consequatur odit repellat accusantium iste modi. Adipisci facere doloremque aliquam debitis magni? Neque ullam molestias mollitia ducimus deserunt eligendi assumenda porro!
          </p>
          <ul class="lista">
            <li v-for="(link, index) in links" :key="index" class="nav">
              {{link.titolo}}
            </li>
          </ul>
          <div class="icona">
            <img src="../img/h12-tabs-icon-1.png" alt="">
          </div>
        </div>
      </div>
    </div>
  </section>
    
</template>

<script>
export default {
  name: 'MainCenter',
  data() {
    return {
      righe: [
        {
          titolo: "What We Do",
          status: true
        },
        {
          titolo: "Degree Programme",
          status: false
        },
        {
          titolo: "Career Achievements",
          status: false
        },
        {
          titolo: "Personal Managment",
          status: false
        },
        {
          titolo: "Steps To Success",
          status: false
        },
        {
          titolo: "Knowledge Transfer",
          status: false
        },
      ],
      links: [
        {
          titolo: "We enrich lives through learning.",
        },
        {
          titolo: "Maximizing potential through individual attention.",
        },
        {
          titolo: "The trusted name for specialized training.",
        },
        {
          titolo: "People thach. People learn. This is where they connect.",
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


.jumbotron {
  height: 800px;
  width: 100%;
  background-image: url('../img/h5-parallax-img-1.png');
  background-repeat: no-repeat;
  background-size: 200%;
  background-position: top, bottom ;
  @include column();
}

.utente {
  width: 100px;
  height: 100px;
}

.utente > img {
  width: 100%;
  border-radius: 50%;
}

.testo {
  width: 50%;
  margin: 80px auto;
  text-align: center;
  color: $bianco;
  @include font22();   
}

.nome {
  margin-bottom: 20px;
  color: $bianco;
  @include font25();
}

.studente {
  color: $bianco;
}

.headerBottom {
    width: 100%;
    height: 50px;
    margin-top: 30px;
    @include justify-content();
  }

  .cerchio {
    margin: 0 5px;
    background: $bianco;
    @include cerchio();
    @include justify-content();
  }

  .info {
    width: 95%;
    height: 700px;
    margin: 0 auto;
    display: flex;
  }

  .celle {
    width: 20%;
    height: 100%;
    @include column();
  }

  .righe {
    width: 100%;
    height: 100px;
    border: 1px solid $griglia;
    @include align-center();
     :hover,
     .active {
          color: #40C4FE;
          border-left: 10px solid #40C4FE;
          height: 100%;
          padding-left: 20px;
          @include align-center();
        }
  }

  .barra {
    padding-left: 30px; 
    color: $lista; 
    @include font22();   
  }
  
  .articolo {
    width: 80%;
    height: 100%;
    @include align-center();
  }

  .titolo {
    position: relative;
    width: 80%;
    height: 90%;
    margin: 0 auto;
    @include araund-column
  }

  .learning {
    @include font50();
  }

  .lorem {
    margin-top: 40px;
    color: $lista; 
    @include font22();
  }

  .lista {
    margin-top: 50px;
  }

  .nav {
    margin: 25px 0;
    list-style: none;
    color: $lista;  
    @include font22();
  }

  .icona {
    position: absolute;
    bottom: 0px;
    right: 0px;
  }


</style>
