<script lang="js">
import {
  Pie
} from 'vue-chartjs'

export default {
  extends: Pie,
  data () {
    return {
      datacollection: {
        labels: [
          'Hardware',
          'Software'
        ],
        datasets: [{
          data: [300, 50],
          backgroundColor: [
            'rgb(88, 208, 222,0.8)',
            'rgb(150, 77, 247,1)'
          ],
          borderColor: [
            'rgb(0,224,147)',
            'rgb(0,143,251)'
          ]
        }]
      },
      options: {
        animateRotate: true,
        animateScale: false,
        responsive: true,
        maintainAspectRatio: true,
        showScale: true,
        legend: {
          display: false
        },
        layout: {
          padding: {
            left: 0,
            right: 0,
            top: 0,
            bottom: 0
          }
        }
      }
    }
  },
  mounted () {
    this.renderChart(this.datacollection, this.options)
  }
}
</script>

<style scoped lang="scss">
.users-doughnut-chart {
}
</style>
