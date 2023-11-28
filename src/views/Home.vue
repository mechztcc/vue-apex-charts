<template>
  <v-container>
    <v-row>
      <v-col cols="6" md="4" lg="4">
        <PieChar />
      </v-col>
      <v-col cols="6" md="4" lg="4">
        <FunelChart />
      </v-col>
      <v-col cols="6" md="4" lg="4">
        <ColumnChart />
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts" setup>
import PieChar from "../components/PieChart.vue";
import FunelChart from "../components/FunelChart.vue";
import ColumnChart from "../components/ColumnChart.vue";
</script>
