
<template>
  <div>
    <div class="bg-img">
      <nav class="navbar fixed-top navbar-expand-lg navbar-dark bg-dark">
        <button
          class="navbar-toggler"
          type="button"
          data-toggle="collapse"
          data-target="#navbarTogglerDemo01"
          aria-controls="navbarTogglerDemo01"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarTogglerDemo01">
          <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
            <li class="nav">
              <a href="#Abortions" style="text-decoration: none;">Abtreibungen 2011 bis 2018</a>
            </li>
            <li class="nav">
              <a href="#Births" style="text-decoration: none;">Geburten 2011 bis 2017</a>
            </li>
            <li class="nav">
              <a href="#Interactive" style="text-decoration: none;">Schwangerschaftsrechner</a>
            </li>
          </ul>
        </div>
      </nav>

      <div
        id="carouselExampleIndicators"
        class="carousel slide"
        data-ride="carousel"
        style="margin-top:40px"
      >
        <ol class="carousel-indicators">
          <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
          <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
          <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
        </ol>
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img class="d-block w-100" src="./assets/title.jpg" alt="First slide">
          </div>
          <div class="carousel-item">
            <img class="d-block w-100" src="./assets/title1.jpg" alt="Second slide">
          </div>
          <div class="carousel-item">
            <img class="d-block w-100" src="./assets/title2.jpg" alt="Second slide">
          </div>
        </div>
        <a
          class="carousel-control-prev"
          href="#carouselExampleIndicators"
          role="button"
          data-slide="prev"
        >
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="sr-only">Previous</span>
        </a>
        <a
          class="carousel-control-next"
          href="#carouselExampleIndicators"
          role="button"
          data-slide="next"
        >
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="sr-only">Next</span>
        </a>
      </div>
    </div>

    <div id="Abortions" class="container-fluid content">
      <div class="row">
        <div class="col-sm-12">
          <h1>Abtreibungen in Deutschland</h1>
          <span class="divider"></span>
        </div>
      </div>
      <div class="row section-content">
        <div class="col-sm-6">
          <h6>Anzahl der Abtreibungen in Deutschland 2011 - 2018</h6>
          <Chart1></Chart1>
        </div>
        <div class="col-sm-6">
          <p>
            Die Anzahl der Abtreibungen in Deutschland ist von 2011 an deutlich gesunken,
            erst in den letzten zwei Jahren ist die Anzahl von Schwangerschaftsabbrüchen wieder
            etwas gestiegen. Die meisten Abbrüche werden dabei bis zur Beendigung der 11 Schwangerschaftswoche
            (SSW) vorgenommen.
            <br>
            <br>2018 haben 97,2 Prozent der Frauen unter der 12 SSW
            einen Schwangerschaftsabbruch vorgenommen. Bei 2,1 Prozent der Frauen war die Schwangerschaft
            schon von der 12. bis 21. SSW vorangeschreitet. Nur bei 0,6 Prozent der Frauen dauererte die Schwangerschaft
            schon mehr als 21 SSW an.
            <br>
            <br>Die meisten Schwangerschaftsabbrüche finden nach der Beratungsregelung statt, selten wird ein Abbruch
            durch medizinische oder kriminologische Indikationen durchgeführt. Zum Beispiel wurde 2018
            97.151 Schwangerschaften durch die Beratungsregelung abgebrochen, 3.815 durch die medizinische
            Indikation und 20 durch die kriminologische Indikation.
            <br>
          </p>
        </div>
      </div>

      <div id="MoreCharts">
        <button
          id="MoreButton"
          data-toggle="collapse"
          data-target="#Abbrueche"
          aria-expanded="false"
          aria-controls="Abbrueche"
        >Weitere Daten einblenden</button>
      </div>
      <div class="collapse" id="Abbrueche">
        <div class="row section-content">
          <div class="col-sm-6">
            <h6>Schwangerschaftsabbrüche nach Dauer der Schwangerschaft in Wochen von 2018</h6>
            <Chart6></Chart6>
          </div>
          <div class="col-sm-6">
            <h6>Schwangerschaftsabrüche nach rechtlicher Begründung von 2011 - 2018</h6>
            <Chart7></Chart7>
          </div>
        </div>
      </div>
    </div>
    <div id="Births" class="container-fluid content grey">
      <div class="row">
        <div class="col-sm-12">
          <h1>Geburten in Deutschland</h1>
          <span class="divider"></span>
        </div>
      </div>
      <div class="row section-content">
        <div class="col-sm-6">
          <p>
            Die Anzahl der Geburten in Deutschland hat von 2011 bis 2016
            einen starken Anstieg vernommen. Von 2016 bis 2017 ist ein leichter Abfall der Geburten
            in Deutschland zu verzeichnen.
            <br>
            <br>Die meisten Frauen bringen einen Jungen auf die Welt. Zum Beispiel kamen 2017
            402.510 Jungen und 382.374 Mädchen auf die Welt. Die meisten Babys werden dabei per Kaiserschnitt
            entbunden. 2017 brachten 232.505 Frauen ihre Babys durch einen Kaiserschnitt auf die Welt.
          </p>
        </div>
        <div class="col-sm-6">
          <h6>Anzahl der Geburten in Deutschland von 2011 - 2017</h6>
          <Chart3></Chart3>
        </div>
      </div>

      <div id="MoreCharts">
        <button
          id="MoreButton"
          data-toggle="collapse"
          data-target="#GebEntb"
          aria-expanded="false"
          aria-controls="GebEntb"
        >Weitere Daten einblenden</button>
      </div>
      <div class="collapse" id="GebEntb">
        <div class="row section-content">
          <div class="col-sm-6">
            <h6>Anzahl der Geburten von Mädchen und Jungen von 2011 - 2017</h6>
            <Chart4></Chart4>
          </div>
          <div class="col-sm-6">
            <h6>Anzahl der Entbindungen durch Kaiserschnitt von 2011 - 2017</h6>
            <Chart5></Chart5>
          </div>
        </div>
      </div>
    </div>

    <div class="container-fluid content green">
      <div class="col-sm-12 questionBox">
        <img id="frage" src="./assets/Frage.png">
        <h2>Weißt du's?</h2>
        <p>
          In Deutschland muss vor einem Schwangerschaftsabbruch eine Beratung in Anspruch genommen werden.
          <br>Bis zu welcher Schwangerschaftswoche glaubst du, kannst du straffrei abtreiben?
        </p>
        <button
          id="1"
          class="qButton"
          @click="answer(false)"
          :disabled="wrongAnswer || rightAnswer == true"
        >Innerhalb 4 Wochen</button>
        <button
          id="2"
          class="qButton"
          @click="answer(false)"
          :disabled="wrongAnswer || rightAnswer == true"
        >Innerhalb 7 Wochen</button>
        <button
          id="RightAnswer"
          class="qButton"
          @click="answer(true)"
          :disabled="wrongAnswer || rightAnswer == true"
        >Innerhalb 12 Wochen</button>
        <button
          id="4"
          class="qButton"
          @click="answer(false)"
          :disabled="wrongAnswer || rightAnswer == true"
        >Innerhalb 15 Wochen</button>
        <p></p>
        <div class="row section-content">
          <div class="col-sm-4"></div>
          <div class="col-sm-4">
            <p v-if="wrongAnswer === true">
              <span style="color:rgb(100,100,100); font-weight: 600;">Diese Antwort ist falsch</span>
              <br>
              <br>In Deutschland bestehen die Regelungen zu Schwangerschaftsabbrüchen seit 1995 im § 218 StGB. Grundsätzlich sind
              <b>Abtreibungen verboten</b> und werden mit bis zu drei Jahren Haft bestraft.
              <br>
              <br>Straffrei wird die Abtreibung erst, nachdem eine Beratung bei einer
              <b>anerkannten Beratungsstelle</b> durchgeführt wurde und seit der Befruchtung nicht mehr als
              <b>zwölf Wochen</b> vergangen sind. Straffrei ist der Abbruch auch, wenn eine
              <b>medizinische oder kriminologische Indikation</b> vorliegt.
            </p>
            <p v-if="rightAnswer === true">
              <span style="color:rgb(100,100,100); font-weight: 600;">Diese Antwort ist richtig</span>
              <br>
              <br>In Deutschland bestehen die Regelungen zu Schwangerschaftsabbrüchen seit 1995 im § 218 StGB. Grundsätzlich sind
              <b>Abtreibungen verboten</b> und werden mit bis zu drei Jahren Haft bestraft.
              <br>
              <br>Straffrei wird die Abtreibung erst, nachdem eine Beratung bei einer
              <b>anerkannten Beratungsstelle</b> durchgeführt wurde und seit der Befruchtung nicht mehr als
              <b>zwölf Wochen</b> vergangen sind. Straffrei ist der Abbruch auch, wenn eine
              <b>medizinische oder kriminologische Indikation</b> vorliegt.
            </p>
          </div>
        </div>
      </div>
    </div>
    <Rechner></Rechner>


    <div class="container-fluid content footer">
      <div class="row">
        <div class="col-sm-12">
          <button id="topButton" title="nach oben">
            <a href="#" style="color: white; text-decoration: none;">
              <img src="./assets/Pfeil.png">
            </a>
          </button>
          <p>A project by Grit Ludwig, Anne Westphal & Anna Tarrach</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Chart1 from "@/Chart1.vue";
import Chart3 from "@/Chart3.vue";
import Chart4 from "@/Chart4.vue";
import Chart5 from "@/Chart5.vue";
import Chart6 from "@/Chart6.vue";
import Chart7 from "@/Chart7.vue";
import Rechner from "@/Rechner.vue";

export default {
  name: "app",
  created() {
    document.title = "Abtreibungen & Geburten in Deutschland";
  },

  data() {
    return {
      rightAnswer: false,
      wrongAnswer: false

    };
  },
  methods: {
    answer(answer) {
      if (answer == false) {
        this.wrongAnswer = true;
      } else {
        this.rightAnswer = true;
      }
    }
  },
  components: {
    Chart1,
    Chart3,
    Chart4,
    Chart5,
    Chart6,
    Chart7,
    Rechner
  }
};

window.onscroll = function() {
  scrollFunction();
};

function scrollFunction() {
  if (document.body.scrollTop > 150 || document.documentElement.scrollTop > 150) {
    document.getElementById("topButton").style.display = "block";
  } else {
    document.getElementById("topButton").style.display = "none";
  }
}
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Montserrat:300,400,500,700|Open+Sans:300,300i,400,400i,700,700i");

html,
body {
  font-family: "Open Sans", sans-serif;
  color: rgb(37, 37, 37);
  font-size: 11pt;
  line-height: 18pt;
}

.nav {
  font-size: 11pt;
  padding-right: 25px;
  padding-top: 10px;
  padding-bottom: 10px;
}

.nav a {
  color: white;
  margin: auto;
}

.nav a:hover {
  color: rgb(19, 216, 203);
}

h1 {
  font-size: 22pt;
  font-weight: 300;
  color: rgb(37, 37, 37);
  text-align: center;
}

h2 {
  font-size: 16pt;
  font-weight: 300;
  color: rgb(100, 100, 100);
  margin-bottom: 15px;
}

h6 {
  font-size: 8pt;
  font-weight: 300;
  text-align: center;
  color: rgb(100, 100, 100);
}

ul {
  list-style: none;
}

#calc {
  font-size: 14pt;
  font-weight: 600;
  line-height: 25pt;
  text-align: center;
  color: rgb(100, 100, 100);
}

#answer {
  font-size: 16pt;
  font-weight: 300;
  line-height: 18pt;
  text-align: center;
  color: #b404ae;
}

.project {
  position: relative;
}

.section-content {
  margin-top: 50px;
}

.grey {
  background-color: rgb(248, 249, 250);
}

.green {
  background-color: rgb(19, 216, 203);
}

#frage {
  width: 15%;
}

.questionBox {
  background-color: white;
  padding: 30px;
  text-align: center;
  border-radius: 5px;
  box-shadow: 5px 5px 15px rgb(66, 66, 66);
}

.content {
  padding-bottom: 50px;
  padding-top: 50px;
}

.divider {
  display: block;
  width: 60px;
  height: 3px;
  background: rgb(19, 216, 203);
  margin: 0 auto;
  margin-top: 15px;
}
.footer {
  font-size: 8pt;
  color: rgb(100, 100, 100);
  text-align: center;
  padding-top: 20px;
}

.active {
  display: block;
}
.inactive {
  display: none;
}

#MoreCharts {
  text-align: center;
}

#MoreButton {
  border: none;
  background-color: rgb(19, 216, 203);
  border-radius: 5px;
  font-size: 18px;
  color: white;
  height: 35px;
  width: 250px;
}

#StichtagButton {
  border: none;
  background-color: rgb(19, 216, 203);
  border-radius: 5px;
  font-size: 18px;
  color: white;
  height: 35px;
  width: 190px;
}

#StichtagButton:hover {
  border: none;
  background-color: rgb(13, 151, 142);
  border-radius: 5px;
  font-size: 18px;
  color: white;
  height: 35px;
  width: 190px;
}

#StichtagButton:focus {
  outline: none;
}
#MoreButton:focus {
  outline: none;
}

.qButton {
  border: none;
  background-color: #343a40;
  border-radius: 5px;
  font-size: 18px;
  color: white;
  height: 35px;
  width: 190px;
  margin-right: 40px;
  margin-top: 10px;
}

.qButton:focus {
  outline: none;
}

.qButton:hover {
  border: none;
  background-color: #b404ae;
  border-radius: 5px;
  font-size: 18px;
  color: white;
  height: 35px;
  width: 190px;
  margin-right: 40px;
}

#MoreButton:hover {
  border: none;
  background-color: rgb(13, 151, 142);
  border-radius: 5px;
  font-size: 18px;
  color: white;
  height: 35px;
  width: 250px;
}

#topButton {
  text-decoration: none;
  display: inline-block;
  position: fixed;
  bottom: 20px;
  right: 30px;
  z-index: 99;
  border: none;
  outline: none;
  background-color: rgb(19, 216, 203);
  color: white;
  cursor: pointer;
  padding: 10px;
  border-radius: 30px;
  font-size: 18px;
}

#topButton:hover {
  background-color: rgb(13, 151, 142);
}

button:disabled {
  background-color: #b404ae;
}

#RightAnswer:disabled {
  background-color: rgb(19, 216, 203);
}

.ErgebnisAnzeigen{
  display: block;
}
.ErgebnisNichtAnzeigen{
  display: none;
}
</style>


