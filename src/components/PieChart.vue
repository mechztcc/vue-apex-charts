<template>
  <apexchart
    :type="chartOptions.chart.type"
    width="380"
    :options="chartOptions"
    :series="series"
  ></apexchart>
</template>
<script setup lang="ts">
import { ref } from "vue";

const series = ref([20, 55, 13, 43, 22]);
const chartOptions = ref({
  chart: {
    type: "donut",
  },
  labels: ["Team A", "Team B", "Team C", "Team D", "Team E"],
  responsive: [
    {
      breakpoint: 480,
      options: {
        chart: {
          width: 400,
        },
        legend: {
          position: "bottom",
        },
      },
    },
  ],
});
</script>
<style lang="scss"></style>
