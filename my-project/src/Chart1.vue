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
        ["1996", 130330],
        ["1997", 130446],
        ["1998", 131372],
        ["1999", 130039],
        ["2000", 134238],
        ["2001", 134462],
        ["2002", 129918],
        ["2003", 127495],
        ["2004", 129164],
        ["2005", 123502],
        ["2006", 119198],
        ["2007", 116315],
        ["2008", 113760],
        ["2009", 110036],
        ["2010", 109506],
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
        title: "Anzahl der Abtreibungen in Deutschland 1996 - 2018",
        backgroundColor: "white",
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

