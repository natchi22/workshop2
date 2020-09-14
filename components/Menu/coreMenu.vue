<template>
  <a-layout
    id="components-layout-demo-side"
    style="min-height: 100vh; position: relative;"
  >
    <a-layout-sider
      v-model="collapsed"
      class="sider"
      theme="light"
      width="256"
      collapsible
      :trigger="null"
    >
      <div class="box">
        <h2>SaaS</h2>
        <h2 v-if="!collapsed">
          Kit
        </h2>
      </div>
      <div class="profile">
        <img
          src="~assets/images/layout/profile_photo.png"
          alt="รูปโปรไฟล์"
        >
        <div class="contact-profile">
          <h3 v-if="!collapsed">
            Sierra Ferguson
          </h3>
          <h4 v-if="!collapsed">
            s.ferguson@gmail.com
          </h4>
        </div>
      </div>
      <a-menu
        :default-selected-keys="['1']"
        mode="inline"
        class="menu"
      >
        <a-menu-item key="1">
          <nuxt-link to="/dashboard">
            <a-icon type="appstore" />
            <span>Dashboard</span>
          </nuxt-link>
        </a-menu-item>

        <a-menu-item key="2">
          <a-icon type="read" />
          <span>Tasks</span>
        </a-menu-item>
        <a-menu-item key="3">
          <a-icon type="mail" />
          <span>Email</span>
        </a-menu-item>
        <a-menu-item key="4">
          <nuxt-link to="/contact">
            <a-icon type="user" />
            <span>Contacts</span>
          </nuxt-link>
        </a-menu-item>
        <a-menu-item key="5">
          <a-icon type="message" />
          <span>Chat</span>
        </a-menu-item>
        <a-menu-item key="6">
          <a-icon type="switcher" />
          <span>Deals</span>
        </a-menu-item>
        <a-menu-item key="7" class="line-setting">
          <a-icon type="ellipsis" />
          <span>Settings</span>
        </a-menu-item>
      </a-menu>
      <!-- <a-icon
        class="trigger"
        :type="collapsed ? 'menu-unfold' : 'menu-fold'"
        @click="() => (collapsed = !collapsed)"
      /> -->
      <div class="trigger" @click="() => (collapsed = !collapsed)">
        <img v-if="!collapsed" src="~assets/images/layout/toggle.png" alt="">
        <img v-if="collapsed" src="~assets/images/layout/toggle-active.png" alt="">
        <p v-if="!collapsed">
          Toggle sidebar
        </p>
      </div>
    </a-layout-sider>
  </a-layout>
</template>
<script>
export default {
  data () {
    return {
      collapsed: false
    }
  }
}
</script>

<style>
.trigger {
  position: fixed;
  display: flex;
  bottom: 0;
  padding: 0 0 22px 27px;
  width: 256px;
}
.trigger p{
  color: #90A0B7;
  font-weight: 500;
  font-size: 11px;
  line-height: 16px;
  margin: 0 0 0 14px;
}
.trigger img{
  width: 14px;
  height: 14px;
}
#components-layout-demo-side .logo {
  height: 32px;
  background: rgba(255, 255, 255, 0.2);
  margin: 16px;
}
.profile {
  display: flex;
  padding: 24px 0 30px 24px;
  border-top: 1px solid #EBEFF2;
}
.profile img {
  width: 46px;
  height: 46px;
  margin-right: 16px;
}
.profile h3 {
  color: #192a3e;
  font-weight: 500;
  font-size: 14px;
  line-height: 21px;
}
.profile h4 {
  color: #90a0b7;
  font-weight: 500;
  font-size: 11px;
  line-height: 16px;
  letter-spacing: 0.01em;
}
.box{
  display: flex;
  padding: 17px 0 17px 24px;
}
.box h2 {
  color: #109cf1;
  font-weight: 600;
  font-size: 18px;
  line-height: 25px;
  margin: 0;
  margin-right: 5px;
}
.box-menu {
  display: flex;
  align-items: center;
  padding: 10px 0 10px 24px ;
}
.box-menu p {
  margin: 0;
  margin-left: 14px;
}
.menu{
 color : #334D6E;
}
.menu li{
  background-color: #ffffff !important;
}
.menu li i{
  color: #C2CFE0;
}
.ant-menu-inline .ant-menu-item::after{
    border-right:none ;
}
.line-setting{
  border-top: 1px solid #EBEFF2;
}
.sider{
  box-shadow: 6px 0px 18px rgba(0, 0, 0, 0.06);
}
.header{
  background-color: #ffffff ;
}
.content{
  display: flex;
}
.content-date{
  width: 100%;
  margin-right: 30px;
}
.ant-layout-sider-light .ant-layout-sider-trigger{
    color: #90A0B7;
}
.ant-layout-sider-trigger{
    text-align: left;
    padding-left: 27px;
}
.ant-menu-vertical{
  border-right: 0px solid #ffffff;
}
.ant-menu-item:hover i, .ant-menu-item:hover span {
  color: #109CF1;
}

.ant-menu-item.ant-menu-item-selected i{
  color: #109CF1 ;
}
</style>
