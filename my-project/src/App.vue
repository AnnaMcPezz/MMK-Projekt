
<template>
  <div>
    <div class="container-fluid header">
      <div class="row">
        <div class="col-sm-12"></div>
      </div>
    </div>

    <div class="bg-img">
      <nav class="navbar navbar-expand-lg navbar-light bg-light">
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
            <li class="nav-item">
              <a class="nav-link" href="#Abortions">Abtreibungen XXXX bis XXXX</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#Births">Geburten blablaaa</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#Interactive">Interaktive Grfafik blaa</a>
            </li>
          </ul>
        </div>
      </nav>
      <div class="header-text">
        <h1 style="color: #fff; font-size:40pt">Titel, Slogan</h1>
        <p style="font-size: 20pt; font-weight: 200">kurzer Text</p>
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
          <Chart1></Chart1>
        </div>
        <div class="col-sm-6">
          <h2>Lorem ipsum dolor sit amet</h2>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
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
          <Chart3></Chart3>
        </div>
       </div>
       <div id="MoreCharts">
       <button @click="MoreChart()">More Charts</button>
       </div>
      <div class="row section-content">
        <div class="col-sm-6">
          <Chart4 v-bind:class="{active: chartActive, inactive: chartInactive }"></Chart4>
        </div>
        <div class="col-sm-6">
          <Chart5 v-bind:class="{active: chartActive, inactive: chartInactive }"></Chart5>
        </div>
      </div>
    </div>
    <div id="Interactive" class="container-fluid content">
      <div class="row">
        <div class="col-sm-12">
          <h1>Interactive form</h1>
          <span class="divider"></span>
        </div>
      </div>
      <div class="row section-content">
        <div class="col-sm-6" id="PregnancyChart">
          <Chart2 v-bind:class="{active: chartActive, inactive: chartInactive }"></Chart2>
        </div>
        <div class="col-sm-6">
          <h2>What is going on in your Pregnancy?
          </h2>
              <p> Gender: 
              <select name="Gender" form="pregnancyForm">
                <option value="unknown">unkown</option>
                <option value="male">male</option>
                <option value="female">female</option>
               </select>
            </p>
            <p> Week of Pregnancy
              <select name="Week of Pregnancy" form="pregnancyForm">
                <option value="1">1</option>
                <option value="2">2</option>
                <option value="3">3</option>
                <option value="4">4</option>
                <option value="5">...</option>
              </select>
            </p>
              <button @click="ShowChart()">Show Chart</button>
        </div>
      </div>
    </div>

    <div class="container-fluid content footer">
      <div class="row">
        <div class="col-sm-12">
          <p>A project by Grit Ludwig, Anne Westphal & Anna Tarrach</p>
        </div>
      </div>
    </div>
    <button onclick="scrollToTop()" id="topButton" title="Go to top"><span class="glyphicon glyphicon-menu-up"></span>Top</button>

  </div>
</template>

<script>
import Chart1 from "@/Chart1.vue";
import Chart2 from "@/Chart2.vue";
import Chart3 from "@/Chart3.vue";
import Chart4 from "@/Chart4.vue";
import Chart5 from "@/Chart5.vue";

export default {
  data() {
    return {
      chartInactive: true,
      chartActive: false
    };
  },
  methods:{
    ShowChart(){
      this.chartActive = true; 
      this.chartInactive = false; 
    },
    MoreChart(){
     this.chartActive = true; 
     this.chartInactive = false; 
    }
  },
  components: {
    Chart1,
    Chart2,
    Chart3,
    Chart4,
    Chart5

  }
};


window.onscroll = function() {scrollFunction()};

function scrollFunction() {
  if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
    document.getElementById("topButton").style.display = "block";
  } else {
    document.getElementById("topButton").style.display = "none";
  }
}

function scrollToTop() {
  document.body.scrollTop = 0;
  document.documentElement.scrollTop = 0; 
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

.image {
  width: 100%;
}

.header {
  padding: 0px;
  position: absolute;
}

.header-text {
  color: #fff;
  text-align: center;
  padding-top: 300px;
  font-size: 30pt;
}
.bg-img {
  background-image: url("./assets/title.jpg");
  min-height: 550px;
  background-position: center;
  background-size: cover;
  position: relative;
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

.project {
  position: relative;
}
.section-content {
  margin-top: 50px;
}

.grey {
  background-color: rgb(248, 249, 250);
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

#MoreCharts{
  text-align: center;
}

#topButton {
  display: none;
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

