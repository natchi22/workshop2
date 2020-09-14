<template>
  <a-layout>
    <a-layout-header class="header">
      <a-input
        placeholder="Global search"
        style="border: none"
      >
        <a-icon
          slot="prefix"
          type="search"
          style="color: #C2CFE0"
        />
        <img src="~assets/images/layout/notifications.png" alt="กระดิ่ง">
      </a-input>
    </a-layout-header>
  </a-layout>
</template>

<style>
.header{
  width: 100%;
  height: 60px;
}
.ant-input{
  border: 0;
}
.ant-input:hover{
  border-color: #ffffff;
}
@media screen and (max-width: 767px){
.ant-layout-header{
  padding: 0 10px;
}
}
</style>
