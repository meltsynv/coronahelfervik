<template>
  <q-page class>
    <section class="intro-section box1">
      <div class="intro-bg"></div>
      <h1 class="title">Gemeinsam Helfen</h1>
      <div class="flex justify-between intro-cards">
        <router-link class="card-link" to="/helfen">
          <q-card class="my-card">
            <img src="../statics/img/home_intro_hilfe_anbieten_small.png" />
            <q-card-section>
              <div class="text-h6 intro-card-text">ICH BRAUCHE HILFE</div>
            </q-card-section>
          </q-card>
        </router-link>
        <router-link class="card-link" to="/helfen">
          <q-card class="my-card">
            <img src="../statics/img/home_intro_hilfe_suchend_small.png" />
            <q-card-section>
              <div class="text-h6 intro-card-text">ICH BRAUCHE HILFE</div>
            </q-card-section>
          </q-card>
        </router-link>
      </div>
      <div class="mouse">
        <div class="scroll"></div>
      </div>
    </section>

    <section class="regionale-suche-section">
      <div class="fit row wrap justify-evenly items-start content-start">
        <img width="30%" src="../assets/Logo.svg" />
      </div>
      <div class="titlediv">
        <h1 class="title">Portal für Nachbarschaftshilfe in deiner Region</h1>
        <i>“Aus der Region - für die Region”</i>
      </div>
      <div class="region-body">
        <h3 class="subtitle">Worum geht es?</h3>
        <p>
          Die aktuelle Situation stellt die Gesellschaft vor neue
          Herausforderungen. Das neuartige Coronavirus hat unser Zusammenleben in
          den vergangenen Wochen zunehmend eingeschränkt. Wir haben das Projekt
          CoronaHelfer ins Leben gerufen, um gemeinsam die Ausbreitung des Virus
          zu verlangsamen und einander dort zu unterstützen, wo es möglich ist.
        </p>
      </div>
      <Regionalesuche/>
    </section>

    <section class="zielundvision-section box2">
      <div class="intro-bg"></div>
      <h1 class="title">ZIEL UND VISION DER INITIATIVE CORONAHELFER</h1>
      <div class="flex justify-between cards">
        <q-card class="my-card">
          <img src="../assets/elderly-people-294088.svg" />
          <q-card-section>
            <div class="text-h6 intro-card-text">schützt gefährdete Personen</div>
          </q-card-section>
        </q-card>
        <q-card class="my-card">
          <img src="../assets/entlastet Menschen.svg" />
          <q-card-section>
            <div class="text-h6 intro-card-text">entlastet Menschen in systemrelevanten Berufen</div>
          </q-card-section>
        </q-card>
        <q-card class="my-card">
          <img src="../assets/children-1296800.svg" />
          <q-card-section>
            <div class="text-h6 intro-card-text">unterstütz Hilfesuchende</div>
          </q-card-section>
        </q-card>
        <q-card class="my-card">
          <img src="../assets/volunteer.svg" />
          <q-card-section>
            <div class="text-h6 intro-card-text">Nachbarschaftshilfe für alle!</div>
          </q-card-section>
        </q-card>
      </div>
    </section>

    <section class="leitsaetze-section">
      <h1 class="title">LEITSÄTZE FÜR CORONAVIRUS-NACHBARSCHAFTSHILFE</h1>
      <div class="leitsaetze-body">
        <div
          v-for="item in items"
          :key="item.img"
          class="principles row q-pa-lg q-mb-lg justify-between items-center"
        >
          <h2 class="principle-sentences">{{(item.principle) }}</h2>
          <img width="40" :src="`statics/icons/${item.img}.svg`" />
        </div>
      </div>
    </section>
    
    <Seperator/>
    
    <section class="unserhintergrund-section">
      <h1 class="title">Unser Hintergrund</h1>
      <p>
        Wie ist unsere Idee entstanden? Über soziale Netzwerke sind wir darauf
        aufmerksam geworden, wie unfassbar viele von euch in ihrer Umgebung
        Hilfe angesichts der aktuellen Situation anbieten möchten. Bei anderen
        Vermittlungsportalen fiel uns die große Anzahl an hilfsbereiten Menschen
        im Gegensatz zu nur wenigen Anfragen auf.
        <br />
        <br />Wir haben erkannt, dass die Vermittlung von Fremden an Fremde eine große
        Herausforderung darstellt und machten uns die Sicherheit unserer Nutzer
        zur Aufgabe. Auch eine verlässliche und schnelle Vermittlung sowie die
        Einbindung bereits bestehender Offline-Arbeit vor Ort sind uns bei der
        Coronavirus-Nachbarschaftshilfe wichtig.
        <br />
        <br />Dank des Hackathons #WirVsVirus der Bundesregierung haben wir ein tolles
        Team für unsere Idee gewinnen können. Seitdem arbeiten wir gemeinsam auf
        Hochtouren an der Umsetzung und dem Ausbau unserer Vermittlungsplattform
      </p>
    </section>
  </q-page>
</template>

<script>
import Regionalesuche from 'components/Regionalesuche';
import Seperator from 'components/Seperator';
export default {
  components:{
    Regionalesuche,
    Seperator
  },
  name: "PageIndex",
  data: () => {
    return {
      items: [
        {
          img: "cool",
          principle: "Cool bleiben"
        },
        {
          img: "Out line",
          principle: "Ordentlich Hände waschen"
        },
        {
          img: "buyer",
          principle: "Rücksichtsvoll bleiben"
        },
        {
          img: "hamster",
          principle: "Ohne Hamsterkäufe"
        },
        {
          img: "help",
          principle: "Nachbarschaftshilfe"
        },
        {
          img: "distance",
          principle: "Abstand halten"
        }
      ]
    };
  }
};
</script>

<style lang="scss">
.title {
  color: $primary;
  text-align: center;
  font-size: 37px;
  font-weight: bold;
  text-transform: uppercase;
}
.subtitle {
  font-size: 20px;
  color: $primary;
  margin-bottom: 0px;
  line-height: initial;
}
p {
  font-size: 20px;
}
.box1 {
  width: 100%;
  height: 80vh;
  overflow: hidden;
  position: relative;
  .intro-bg {
    width: 200%;
    height: 80vh;
    background-color: #fff3e9;
    transform: rotateZ(-2deg);
    position: absolute;
    top: -5%;
    left: -50%;
    z-index: -1;
  }
}
.box2 {
  width: 100%;
  height: auto;
  position: relative;
  overflow: hidden;
  padding-bottom: 200px;
  padding-top: 100px;
  .intro-bg {
    width: 110%;
    height: 90%;
    background-color: $background;
    transform: rotateZ(-2deg);
    position: absolute;
    top: 5%;
    left: -5%;
    z-index: -1;
  }
}
.intro-section {
  .intro-cards {
    margin: 0 auto;
    width: 65%;
    .card-link {
      width: 43%;
      text-decoration: none;
      transition: 300ms ease-out;
      &:hover {
        transform: scale(1.01);
        box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.1);
      }
      .my-card {
        text-align: center;
        .intro-card-text {
          color: $primary;
          font-weight: bold;
        }
      }
    }
  }
  .mouse {
    width: 35px;
    height: 50px;
    border-radius: 25px;
    border: 2px solid $secondary;
    position: absolute;
    bottom: 100px;
    left: 50%;
    transform: translate(-50%);
    opacity: 0.3;
    .scroll {
      width: 2px;
      height: 10px;
      margin: 0 auto;
      margin-top: 5px;
      border-radius: 5px;
      background-color: $secondary;
      animation-name: scroll;
      transition: 800ms ease-in-out;
      animation-duration: 1s;
      animation-iteration-count: infinite;
    }
  }
  @keyframes scroll {
    from {
      margin-top: 5px;
    }
    to {
      margin-top: 10px;
    }
  }
}
.regionale-suche-section {
  width: 65%;
  margin: 0 auto;
  margin-top: 100px;
  margin-bottom: 200px;
  .titlediv {
    display: table;
    margin: 0 auto;
    .title {
      margin-bottom: 0px;
      line-height: inherit;
    }
  }
  .region-body {
    margin-top: 70px;
  }
}
.zielundvision-section {
  .cards {
    margin: 0 auto;
    width: 65%;
    .my-card {
      width: 45%;
      margin-top: 50px;
      text-align: center;
      img {
        padding-top: 25px;
        margin: 0 auto;
        width: auto;
        height: 200px;
      }
    }
  }
}
.leitsaetze-section {
  .leitsaetze-body {
    width: 65%;
    margin: 0 auto;
    .principles {
      padding: 10px;
      background-color: $background;
      border-radius: 10px;
      .principle-sentences {
        margin: 10px 0;
        font-size: 37px;
      }
      .principle-sentences::first-letter {
        font-weight: bold;
        color: $primary;
      }
    }
  }
}
.unserhintergrund-section{
  width: 65%;
  margin: 0 auto;
  .title{
    margin-top: 0px;
    line-height: inherit;
  }
}
</style>
