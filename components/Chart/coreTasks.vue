<script>
import { Doughnut } from 'vue-chartjs'

export default {
  extends: Doughnut,
  props: ['tasksdata', 'options'],
  mounted () {
    this.renderChart(this.tasksdata, this.options)
  }
}
</script>
