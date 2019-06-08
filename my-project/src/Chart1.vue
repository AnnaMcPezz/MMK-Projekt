<template>
    <p>
        <GChart 
        type="LineChart" 
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
    name: "Chart1",
    data(){
    return{
    chartData: [
        [
          "Jahr",
          "Abtreibungen"
        ],
        ["2011", 107858],
        ["2012", 105727],
        ["2013", 101710],
        ["2014", 98464],
        ["2015", 98126],
        ["2016", 97772],
        ["2017", 100145],
        ["2018", 99905]

      ],
      chartOptions: {
        title: "Anzahl der Abtreibungen in Deutschland 2011 - 2018",
        backgroundColor: "white",
        animation:{
        duration: 1000,
        startup: 'true',
        easing: 'out'},
        series: {
          0:{color: '#04B4AE'}
          },
        legend: {
          position: 'bottom',
          alignment: 'center'
          },
        }
    }

    },
    components: {
    GChart
  }
}
</script>

