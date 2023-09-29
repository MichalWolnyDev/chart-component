<script setup>
  import { ref } from 'vue'
  import BarChart from './components/BarChart.vue'

  const chartOptions = ref({
    responsive: true
  })

  const chartData = ref({
     labels: [ 'January', 'February', 'March'],
        datasets: [
          {
            label: 'Data One',
            backgroundColor: '#f87979',
            data: [40]
          }
        ]
  })
</script>

<template>
  <BarChart :chartOptions="chartOptions" :chartData="chartData"/>
</template>

<style scoped>

</style>
