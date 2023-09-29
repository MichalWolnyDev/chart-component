<script setup>
  import { ref } from 'vue'
  import BarChart from './components/BarChart.vue'

  const chartOptions = ref({
    responsive: true,
    scales: {
      x: {
        stacked: true
      },
      y: {
        stacked: true
      }
    }
  })

  const chartData = ref({
     labels: [ 'Poniedziałek', 'Wtorek', 'Środa', 'Czwartek', 'Piątek', 'Sobota', 'Niedziela'],
        datasets: [
          {
            type: 'line',
            label: 'Line Dataset',
            data: [40, 20, 30, 15, 80, 100, 10],
            backgroundColor: '#fff',
            borderColor: '#FF8D1C',
            pointRadius: 10,
            pointHoverRadius: 15
          },
          {
            type: 'bar',
            label: 'Bar Dataset',
            backgroundColor: '#f87979',
            borderRadius: 100,
            data: [40, 20, 30, 15, 80, 100, 10]
          },
          {
            type: 'bar',
            label: 'Bar Dataset 2',
            backgroundColor: '#ff0',
            borderRadius: 100,
            data: [40, 20, 30, 15, 80, 100, 10]
          },
          {
            type: 'bar',
            label: 'Bar Dataset 3',
            backgroundColor: '#00f',
            borderRadius: 100,
            data: [40, 20, 30, 15, 80, 100, 10]
          }
        ]
  })
</script>

<template>
  <BarChart :chartOptions="chartOptions" :chartData="chartData"/>
</template>

<style scoped>

</style>
