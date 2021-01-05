<template>
  <canvas :id="chartId" width="400" height="400"></canvas>
</template>

<script>
import Chart from 'chart.js'
import { onMounted, ref } from 'vue'

export default {
  setup() {
    // create a somewhat random id...
    const chartId = ref('chart-' + Math.floor(Math.random() * 100))

    const initChart = () => {
      const ctx = document.getElementById(chartId.value).getContext('2d')
      const myChart = new Chart(ctx, {
        type: 'bar',
        data: {
          labels: ['ETH', 'BTC', 'USDT'],
          datasets: [
            {
              label: 'Allocation',
              data: [12, 19, 3],
              backgroundColor: [
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
              ],
              borderColor: [
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
              ],
              borderWidth: 1,
            },
          ],
        },
        options: {
          scales: {
            yAxes: [
              {
                ticks: {
                  beginAtZero: true,
                },
              },
            ],
          },
        },
      })
    }

    onMounted(() => {
      initChart()
    })

    return { chartId }
  },
}
</script>
