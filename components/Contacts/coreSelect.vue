<template>
  <div class="company">
    <P>Company:</P>
    <a-select default-value="all" @change="handleChange">
      <a-select-option value="all">
        All
      </a-select-option>
      <a-select-option value="hatchbuck">
        Hatchbuck
      </a-select-option>
      <a-select-option value="google">
        Google
      </a-select-option>
      <a-select-option value="upwork">
        Upwork
      </a-select-option>
      <a-select-option value="facebook">
        Facebook
      </a-select-option>
    </a-select>
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
</style>
