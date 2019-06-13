<template>
  <p>
    <GChart type="PieChart" :data="chartData" :options="chartOptions"/>
  </p>
</template>

<script>
import Vue from "vue";
import VueGoogleCharts from "vue-google-charts";

Vue.use(VueGoogleCharts);

import { GChart } from "vue-google-charts";

export default {
  name: "Chart1",
  data() {
    return {
      chartData: [
        ["Schwangerschaftswoche", "Schwangerschaftswoche"],
        ["1", 100],
        ["2", 200],
        ["3", 300],
        ["4", 400]
      ],
      chartOptions: {
        title: "Schwangerschaftswoche",
        pieHole: 0.6,
        backgroundColor: "white",
        animation: {
          duration: 1000,
          easing: "out"
        }
      }
    };
  },
  components: {
    GChart
  }
};
</script>

