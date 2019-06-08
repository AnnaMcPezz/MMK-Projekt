<template>
    <p>
        <GChart 
        type="PieChart" 
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
    name: "Chart5",
    data(){
    return{
    chartData: [
        [
          "Jahr",
          "Kaiserschnitt"
        ],
        ["2011",  206791],
        ["2012",  208254],
        ["2013",  210570],
        ["2014",  220540],
        ["2015",  222919],
        ["2016",  232479],
        ["2017",  232505]       

      ],
      chartOptions: {
        title: "Anzahl der Entbindungen durch Kaiserschnitt von 2011 - 2018",
        pieHole: 0.3,
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

