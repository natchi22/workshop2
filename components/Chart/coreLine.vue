<template>
  <div>
    <div class="lineprogress">
      <div class="task-top">
        <div class="completed">
          <p>Deals</p>
        </div>
        <div class="company">
          <p>Show:</p>
          <a-select default-value="Monthly" @change="handleChange">
            <a-select-option value="Monthly">
              Monthly
            </a-select-option>
          </a-select>
        </div>
      </div>
    </div>
    <coreDeals class="coredeals" :chartdata="datacollection" :options="options" />
  </div>
</template>
<script>
import coreDeals from '@/components/Chart/coreDeals'
export default {
  components: {
    coreDeals
  },
  data () {
    return {
      datacollection: {
        labels: ['1 Dec', '8 Dec', '16 Dec', '31 Dec'],
        datasets: [
          {
            label: '', // Closed deals
            borderColor: '#109CF1',
            backgroundColor: 'rgba(16, 156, 241, 0.2)',
            data: [60, 170, 140, 150],
            borderWidth: '2',
            lineTension: '0.9'
          }
        ]
      },
      options: {
        legend: {
          display: false
        }
      }
    }
  },
  methods: {
    handleChange (value) {
    //   console.log(`selected ${value}`)
    }
  }
}
</script>
<style scoped>
.lineprogress{
    background-color: #fff;
padding: 0 24px;
border-bottom:1px solid #EBEFF2 ;
border-radius:  4px 4px 0 0;
height: 54px;
/* align-items: center; */
}
.completed{
    display: flex;
    color: #192A3E;
    font-weight: 500;
    margin: auto 0;
    height: 19px;
}
.completed p{
font-size: 15px ;
    margin: 0;
}
.task-top{
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 54px;
}
.company{
  display: flex;
  align-items: center;
}
.company  p{
  font-size: 12px;
  color: #6A707E;
  margin: 0;
}
.ant-select-selection-selected-value{
  color: #109CF1;
  font-size: 12px;

}
.ant-select-selection{
  background-color: transparent;
  border: none;
  width: 100px;
}
.ant-select-focused .ant-select-selection, .ant-select-selection:focus, .ant-select-selection:active{
 box-shadow: none !important;
}
.ant-select-dropdown-menu-item{
  color: #6A707E;
  font-size: 12px;
}
.coredeals .chartjs-size-monitor .chartjs-render-monitor{
margin: 0 auto !important;
}
</style>
