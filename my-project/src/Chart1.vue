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
          "Year",
          "Sales",
          "Expenses",
          { role: "style" },
          "Profit",
          { role: "style" },
    
        ],
        ["2014", 200, 200, "black", 200, "black"],
        ["2015", 200, 200, "black", 250, "black"],
        ["2016", 200, 1120, "black", 300, "black"],
        ["2017", 200, 540, "black", 350, "black"]
      ],
      chartOptions: {
        title: "Company Performance",
        backgroundColor: "white",
        animation:{
        duration: 1000,
        startup: 'true'}
        }
    }

    },
    components: {
    GChart
  }
}
</script>

