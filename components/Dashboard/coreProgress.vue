<template>
  <div class="progress">
    <div class="task-top">
      <div class="completed">
        <p>8 task completed out of 10</p>
      </div>
      <div class="company">
        <p>Show:</p>
        <a-select default-value="This week" @change="handleChange">
          <a-select-option value="This week">
            This week
          </a-select-option>
        </a-select>
      </div>
    </div>

    <a-progress
      :percent="80"
      :show-info="false"
    />
  </div>
</template>
<script>
export default {
  methods: {
    handleChange (value) {
      console.log(`selected ${value}`)
    }
  }
}
</script>
<style>
.progress{
    background-color: #fff;
    padding: 0 24px;
}
.ant-progress-bg{
    background-color: #2ED47A;
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
@media screen and (max-width: 1279px ) and (min-width: 768px ){

}
@media screen and (max-width: 767px){
.task-top{
  flex-direction: column;
}
}
</style>
