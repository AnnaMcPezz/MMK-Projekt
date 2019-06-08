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
        pieHole: 0.3,
        backgroundColor: "#FAFAFA",
        animation:{
        duration: 1000,
        startup: 'true',
        easing: 'out'},
        pieSliceText: 'none',
        legend: {
            position: 'bottom'
              },
        slices: {
                0: {
                  color: '#0B615E'
                },
                1: {
                  color: '#088A85'
                },
                2: {
                  color: '#04B4AE'
                },
                3: {
                  color: '#01DFD7'
                },
                4: {
                  color: '#A901DB'
                },
                5: {
                  color: '#8904B1'
                },
                6: {
                  color: '#6A0888'
                }
              }
        }
    }

    },
    components: {
    GChart
  }
}
</script>

