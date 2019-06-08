<template>
    <p>
        <GChart 
        type="BarChart" 
        :data="chartData" 
        :options="chartOptions"
        />
    </p>
</template>

<script>

import Vue from "vue";
import VueGoogleCharts from "vue-google-charts";

Vue.use(VueGoogleCharts);

import { GChart } from "vue-google-charts";

export default {
    name: "Chart4",
    data(){
    return{
    chartData: [
        [
          "Jahr",
          "Mädchen",
          "Jungen"
        ],
        ["2011", 322786, 339899],
        ["2012", 327915, 345629],
        ["2013", 332249, 349820],
        ["2014", 348092, 366835],
        ["2015", 359097, 378478],
        ["2016", 386546, 405585],
        ["2017", 382374, 402510]       

      ],
      chartOptions: {
        title: "Anzahl der Geburten von Mädchen & Jungen von 2011 - 2018",
        backgroundColor: "#FAFAFA",
        animation:{
        duration: 1000,
        startup: 'true',
        easing: 'out'}
        }
    }

    },
    components: {
    GChart
  }
}
</script>

