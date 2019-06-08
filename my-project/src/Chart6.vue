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
    name: "Chart6",
    data(){
    return{
    chartData: [
        [
          "Schwangerschaftswoche",
          "Anzahl"
        ],
        ["unter 12", 98168],
        ["12 bis 21", 2163],
        ["22 und mehr", 655]     

      ],
      chartOptions: {
        legend: {
                position: 'bottom',
                alignment: 'center'
              },
        backgroundColor: "white",
        bars: 'vertical',
        slices: {
          0:{color: '#B404AE'},
          1:{color: '#04B4AE', offset: 0.3},
          2:{color: '#0B615E', offset: 0.5}
          },
        pieSliceText: 'none',
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

