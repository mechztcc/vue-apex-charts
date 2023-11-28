<template>
  <apexchart :type="chartOptions.chart.type" height="350" :options="chartOptions" :series="series"></apexchart>
</template>
<script setup lang="ts">
import { ref } from "vue";

const series = ref([
  {
    name: "Funnel Series",
    data: [1380, 1100, 990, 880, 740, 548, 330, 200],
  },
]);

const chartOptions = ref({
  chart: {
    type: "bar",
    height: 350,
  },
  plotOptions: {
    bar: {
      borderRadius: 5,
      horizontal: true,
      barHeight: "80%",
      isFunnel: true,
    },
  },
  dataLabels: {
    enabled: true,
    formatter: function (val: any, opt: any) {
      return opt.w.globals.labels[opt.dataPointIndex] + ":  " + val;
    },
    dropShadow: {
      enabled: true,
    },
  },
  title: {
    text: "Recruitment Funnel",
    align: "middle",
  },
  xaxis: {
    categories: [
      "Sourced",
      "Screened",
      "Assessed",
      "HR Interview",
      "Technical",
      "Verify",
      "Offered",
      "Hired",
    ],
  },
  legend: {
    show: false,
  },
});
</script>
<style lang=""></style>
