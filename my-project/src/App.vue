
<template>
  <div>
    <div class="container-fluid header">
      <div class="row">
        <div class="col-sm-12"></div>
      </div>
    </div>

    <div class="bg-img">
      <div class="nav-menu">
        <ul id="container-nav">
          <li>
            <a href="#Abortions">Abortions</a>
          </li>
          <li>
            <a href="#Births">Births</a>
          </li>
          <li>
            <a href="#Interactive">Interactive form</a>
          </li>
        </ul>
      </div>
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
          <Chart1></Chart1>
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
        <div class="col-sm-6">
          <Chart1></Chart1>
        </div>
        <div class="col-sm-6">
          <h2>Lorem ipsum dolor sit amet</h2>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
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
  </div>
</template>

<script>
import Chart1 from "@/Chart1.vue";
import Chart2 from "@/Chart2.vue";

export default {
  data() {
    return {};
  },
  components: {
    Chart1,
    Chart2
  }
};
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
.nav-menu {
  text-align: center;
  position: relative;
}
ul#container-nav li {
  display: inline-block;
  margin-left: 35px;
  text-decoration: none;
  padding: 30px 16px;
  font-size: 14px;
}

.nav-menu a {
  color: #fff;
}

.nav-menu a:hover {
  color: rgb(32, 243, 155);
  text-decoration: none;
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
</style>
