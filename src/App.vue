<script setup>
import { ref } from "vue";
import BarChart from "./components/BarChart.vue";

const chartOptions = ref({
  categoryPercentage: 1,
  barPercentage: 0.9,
  borderRadius: 100,
  pointRadius: 3,
  pointHoverRadius: 8,
  responsive: true,
  scales: {
    x: {
      display: false,
      stacked: true,
    },
    y: {
      display: false,
      stacked: true,
    },
  },
  plugins: {
    legend: {
      display: false,
    },
  },
});

const chartData = ref({
  labels: ["Poniedziałek", "Wtorek", "Środa", "Czwartek", "Piątek", "Sobota", "Niedziela"],
  datasets: [
    {
      type: "line",
      label: "Line Dataset",
      data: [140, 220, 130, 115, 180, 100, 210],
      backgroundColor: "#fff",
      borderColor: "#FF8D1C",
    },
    {
      type: "bar",
      label: "Bar Dataset",
      backgroundColor: "#f87979",
      data: [40, 20, 30, 15, 80, 100, 10],
    },
    {
      type: "bar",
      label: "Bar Dataset 2",
      backgroundColor: "#ff0",
      data: [60, 20, 30, 15, 80, 100, 10],
    },
    {
      type: "bar",
      label: "Bar Dataset 3",
      backgroundColor: "#00f",
      data: [40, 20, 30, 15, 80, 100, 10],
    },
  ],
});
</script>

<template>
  <div class="chart">
    <BarChart :chartOptions="chartOptions" :chartData="chartData" />
  </div>
</template>

<style scoped>
.chart{
  max-width: 500px;
}
</style>
