
<template>
  <div>
    <div class="bg-img">
      <nav class="navbar fixed-top navbar-expand-lg navbar-light bg-dark">
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
              <a href="#Abortions" style="text-decoration: none;">Abtreibungen XXXX bis XXXX</a>
            </li>
            <li class="nav">
              <a href="#Births" style="text-decoration: none;">Geburten blablaaa</a>
            </li>
            <li class="nav">
              <a href="#Interactive" style="text-decoration: none;">Interaktive Grafik blaa</a>
            </li>
          </ul>
        </div>
      </nav>

      <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
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
            <img class="d-block w-100" src="./assets/title_2.jpg" alt="Second slide">
          </div>
          <div class="carousel-item">
            <img class="d-block w-100" src="./assets/title_3.jpg" alt="Third slide">
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
          <h1>Abortions</h1>
          <span class="divider"></span>
        </div>
      </div>
      <div class="row section-content">
        <div class="col-sm-6">
          <h6>Anzahl der Abtreibungen in Deutschland 2011 - 2018</h6>
          <Chart1></Chart1>
        </div>
        <div class="col-sm-6">
          <h2>Lorem ipsum dolor sit amet</h2>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
        </div>
      </div>
      <div id="MoreCharts">
        <button id="MoreButton" @click="MoreCharts()">More Charts</button>
      </div>
      <div class="row section-content">
        <div class="col-sm-6">
          <h6
            v-bind:class="{active: chartActive, inactive: chartInactive }"
          >Schwangerschaftsabbrüche nach Dauer der Schwangerschaft von 2018</h6>
          <Chart6 v-bind:class="{active: chartActive, inactive: chartInactive }"></Chart6>
        </div>
        <div class="col-sm-6">
          <h6
            v-bind:class="{active: chartActive, inactive: chartInactive }"
          >Schwangerschaftsabrüche nach rechtlicher Begründung von 2011 - 2018</h6>
          <Chart7 v-bind:class="{active: chartActive, inactive: chartInactive }"></Chart7>
        </div>
      </div>
    </div>
    <div id="Births" class="container-fluid content grey">
      <div class="row">
        <div class="col-sm-12">
          <h1>Births</h1>
          <span class="divider"></span>
        </div>
      </div>
      <div class="row section-content">
        <div class="col-sm-6">
          <h2>Lorem ipsum dolor sit amet</h2>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
        </div>
        <div class="col-sm-6">
          <h6>Anzahl der Geburten in Deutschland von 2011 - 2017</h6>
          <Chart3></Chart3>
        </div>
      </div>
      <div id="MoreCharts">
        <button id="MoreButton" @click="MoreBirthCharts()">More Charts</button>
      </div>
      <div class="row section-content">
        <div class="col-sm-6">
          <h6
            v-bind:class="{active: birthChartActive, inactive: birthChartInactive }"
          >Anzahl der Geburten von Mädchen und Jungen von 2011 - 2017</h6>
          <Chart4 v-bind:class="{active: birthChartActive, inactive: birthChartInactive }"></Chart4>
        </div>
        <div class="col-sm-6">
          <h6
            v-bind:class="{active: birthChartActive, inactive: birthChartInactive }"
          >Anzahl der Entbindungen durch Kaiserschnitt von 2011 - 2017</h6>
          <Chart5 v-bind:class="{active: birthChartActive, inactive: birthChartInactive }"></Chart5>
        </div>
      </div>
    </div>

    <div class="container-fluid content green">
      <div class="col-sm-12 questionBox">
        <h2>Bis zu welcher Schwangerschaftswoche glauben Sie, können Sie in D straffrei abtreiben?</h2>
        <p></p>
        <button id="qButton" value="1" @click="xxx()">4 Wochen</button>
        <button id="qButton" value="1" @click="xxx()">7 Wochen</button>
        <button id="qButton" value="2" @click="xxx()">12 Wochen</button>
        <button id="qButton" value="1" @click="xxx()">15 Wochen</button>
      </div>
    </div>

    <div id="Interactive" class="container-fluid content">
      <div class="row">
        <div class="col-sm-12">
          <h1>Interactive form</h1>
          <span class="divider"></span>
        </div>
      </div>
      <div class="row section-content" style="text-align: center;">
        <div class="col-sm-12" id="PregnancyChart">
          <h2>What is going on in your Pregnancy?</h2>
          <p>
            EinleitungEinleitungEinleitungEinleitungEinleitung
            <br>EinleitungEinleitung Einleitung
          </p>
          <p>
            Erster Tag der Monatsblutung:
            <select name="Monatsblutung" form="pregnancyForm">
              <option value="unknown">unkown</option>
              <option value="male">male</option>
              <option value="female">female</option>
            </select>
          </p>
          <p>
            Zykluslänge
            <select name="Zykluslänge" form="pregnancyForm">
              <option value="1">1</option>
              <option value="2">2</option>
              <option value="3">3</option>
              <option value="4">4</option>
              <option value="5">...</option>
            </select>
          </p>
          <p>
            Value:
            <input type="range" min="0" step="10" max="100" v-model="value">
            {{value}}
          </p>
          <button id="MoreButton" @click="ShowChart()">Show Chart</button>
        </div>

        <div class="col-sm-6" style="margin-top: 40px;">
          <Chart2 v-bind:class="{active: pChartActive, inactive: pChartInactive }"></Chart2>
        </div>
        <div class="col-sm-6" style="margin-top: 40px;">
          <Chart2 v-bind:class="{active: pChartActive, inactive: pChartInactive }"></Chart2>
        </div>
      </div>
    </div>

    <div class="container-fluid content footer">
      <div class="row">
        <div class="col-sm-12">
          <button id="topButton" title="nach oben">
            <a href="#" style="color: white; text-decoration: none;">Top</a>
          </button>
          <p>A project by Grit Ludwig, Anne Westphal & Anna Tarrach</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Chart1 from "@/Chart1.vue";
import Chart2 from "@/Chart2.vue";
import Chart3 from "@/Chart3.vue";
import Chart4 from "@/Chart4.vue";
import Chart5 from "@/Chart5.vue";
import Chart6 from "@/Chart6.vue";
import Chart7 from "@/Chart7.vue";

export default {
  data() {
    return {
      chartInactive: true,
      chartActive: false,
      pChartInactive: true,
      pChartActive: false,
      birthChartActive: false,
      birthChartInactive: true
    };
  },
  methods: {
    ShowChart() {
      this.pChartActive = true;
      this.pChartInactive = false;
    },
    MoreCharts() {
      this.chartActive = true;
      this.chartInactive = false;
    },
    MoreBirthCharts() {
      this.birthChartActive = true;
      this.birthChartInactive = false;
    }
  },
  components: {
    Chart1,
    Chart2,
    Chart3,
    Chart4,
    Chart5,
    Chart6,
    Chart7
  }
};

window.onscroll = function() {
  scrollFunction();
};

function scrollFunction() {
  if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
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
  width: 135px;
}

#qButton {
  border: none;
  background-color: rgb(19, 216, 203);
  border-radius: 5px;
  font-size: 18px;
  color: white;
  height: 35px;
  width: 135px;
  margin-right: 40px;
}

#ButtonWrong {
  border: none;
  background-color: rgb(235, 13, 13);
  border-radius: 5px;
  font-size: 18px;
  color: white;
  height: 35px;
  width: 135px;
  margin-right: 60px;
}

#ButtonRight {
  border: none;
  background-color: rgb(52, 216, 79);
  border-radius: 5px;
  font-size: 18px;
  color: white;
  height: 35px;
  width: 135px;
  margin-right: 60px;
}

#qButton:hover {
  border: none;
  background-color: rgb(13, 151, 142);
  border-radius: 5px;
  font-size: 18px;
  color: white;
  height: 35px;
  width: 135px;
  margin-right: 40px;
}

#MoreButton:hover {
  border: none;
  background-color: rgb(13, 151, 142);
  border-radius: 5px;
  font-size: 18px;
  color: white;
  height: 35px;
  width: 135px;
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
  border-radius: 5px;
  font-size: 18px;
}

#topButton:hover {
  background-color: #555;
}
</style>

