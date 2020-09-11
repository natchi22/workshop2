<template>
  <div>
    <coreLine />
  </div>
</template>

<script>

import coreLine from '@/components/Chart/coreLine'
export default {
  components: {

    coreLine
  },
  data () {
    return {
      datacollection: {
        labels: ['1 Dec', '8 Dec', '16 Dec', '31 Dec'],
        datasets: [
          {
            label: 'Closed deals',
            borderColor: '#109CF1',
            backgroundColor: 'rgba(16, 156, 241, 0)',
            opacity: '0.2',
            data: [60, 170, 140, 150],
            borderWidth: '2',
            lineTension: '0.9'
          }
        ]
      },
      tasks: {
        // labals: ['red', 'green', 'pink'],
        datasets: [{
          label: 'My First Dataset',
          data: [60, 30, 10],
          backgroundColor: [
            '#2ED47A',
            '#FFB946',
            '#F7685B'],
          borderWidth: 0,
          cutoutPercentage: 60

        }]
      }
    }
  }
}
</script>

<style>
.chartjs-render-monitor {
  width: 100% !important;
  height: 100% !important;
}
</style>
