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
    name: "Chart7",
    data(){
    return{
    chartData: [
        [
          "Jahr",
          "Medizinische Indikation",
          "Kriminologische Indikation",
          "Beratungsregelung"
        ],
        ["2011", 3485, 25, 105357],
        ["2012", 3326, 27, 103462],
        ["2013", 3703, 20, 99079],
        ["2014", 3594, 41, 96080],
        ["2015", 3879, 20, 95338],
        ["2016", 3785, 28, 94908],
        ["2017", 3911, 20, 97278], 
        ["2018", 3815, 20, 97151]      

      ],
      chartOptions: {
        legend: {
                position: 'bottom',
                alignment: 'center'
              },
        backgroundColor: "white",
        series: {
          0:{color: '#B404AE'},
          1:{color: '#04B4AE'},
          2:{color: '#01DFD7'}
          },
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

