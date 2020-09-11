<template>
  <div>
    <link rel="stylesheet" href="styledropdown.css">
    <div class="progress">
      <div class="task-top">
        <div class="completed">
          <p>Tasks</p>
        </div>
        <div class="company">
          <p>Show:</p>
          <a-select default-value="This month" @change="handleChange">
            <a-select-option value="This month">
              This month
            </a-select-option>
          </a-select>
        </div>
      </div>
    </div>
    <div class="chart60">
      <div>
        <coreTasks class="coretasks" :tasksdata="tasks" :options="nat" />
      </div>
      <div class="percentage">
        <h1>60%</h1>
      </div>

      <div class="status-text">
        <div class="status-color">
          <img src="~/assets/images/layout/ring1.png" alt="เหลือง">
          <p>Active</p>
        </div>
        <div class="status-color">
          <img src="~/assets/images/layout/ring2.png" alt="เขียว">
          <p>Completed</p>
        </div>
        <div class="status-color">
          <img src="~/assets/images/layout/ring3.png" alt="แดง">
          <p>Ended</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import coreTasks from '@/components/Chart/coreTasks'
export default {
  components: {
    coreTasks
  },
  data () {
    return {

      tasks: {
        // labals: ['red', 'green', 'pink'],
        datasets: [{
          label: 'My First Dataset',
          data: [60, 30, 10],
          backgroundColor: [
            '#2ED47A',
            '#FFB946',
            '#F7685B'],
          borderWidth: 0
        }]
      },
      nat: {
        cutoutPercentage: 93,
        rotation: 2.5

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
.progress{
    background-color: #fff;
    padding: 0 24px;
    border-bottom:1px solid #EBEFF2 ;
    border-radius:  4px 4px 0 0;
    height: 54px;
}
.completed{
    display: flex;
    color: #334D6E;
    font-weight: 500;
    font-size: 13px;
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
.coretasks{
    width: 224px;
    height: 224px;
    margin: 32px 0;
}
.status-color img{
    width: 8px;
    height: 8px;

}
.status-color{
    display: flex;
    align-items: center;
}
.status-color p{
    margin: 0;
    margin-left: 8px;
}
.chart60{
    display: flex;
    justify-content: space-around;
    position: relative;
}
.status-text{
    display: flex;
    flex-direction: column;
    justify-content: center;
}
.percentage{
    display: flex;
align-items: center;
position: absolute;
bottom: 100px;
right: 238px;
}
.percentage h1{
    font-weight: 500;
    font-size: 56px;
    color: #2ED47A;
    height: 82px;
    margin: 0;
}
@media screen and (max-width: 1279px ) and (min-width: 768px ){
.percentage{
bottom: 100px;
right: 428px;
}
}
@media screen and (max-width: 767px){
.percentage{
bottom: 185px;
right: 95px;
}
.chart60{
  display: flex;
  flex-direction: column;
}
.status-color{
  width: 80px;
  margin: 0 auto;
}
.coretasks{
    margin: 0 auto;
}
.status-text{
  margin: 30px 0;
}
}
</style>
