<template>
    <p>
        <GChart 
        type="ColumnChart" 
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
        legend: {
                position: 'bottom',
                alignment: 'center'
              },
        backgroundColor: "#FAFAFA",
        bars: 'vertical',
        series: {
          0:{color: '#B404AE', visibleInLegend: true},
          1:{color: '#04B4AE', visibleInLegend: true}
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

