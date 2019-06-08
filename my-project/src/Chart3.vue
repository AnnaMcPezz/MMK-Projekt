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
    name: "Chart3",
    data(){
    return{
    chartData: [
        [
          "Jahr",
          "Geburten"
        ],
        ["2011", 662685],
        ["2012", 673544],
        ["2013", 682069],
        ["2014", 714927],
        ["2015", 737575],
        ["2016", 792141],
        ["2017", 784901]

      ],
      chartOptions: {
        title: "Anzahl der Geburten in Deutschland von 2011 - 2017",
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

