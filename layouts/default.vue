<template>
  <div class="page">
    <coreMenu />
    <div class="col-head">
      <coreHeader />
      <div class="main">
        <nuxt class="test" />
      </div>
    </div>
  </div>
</template>
<script>
import coreMenu from '@/components/Menu/coreMenu'
import coreHeader from '@/components/Header/coreHeader'
export default {
  components: {
    coreMenu,
    coreHeader

  }

}
</script>
<style>
.test{
  /* position: relative; */
  /* z-index: -1; */
}
div[data-v-6fc4d46b]{
    padding: 0 !important;
    margin: 36px;
    background-color: #ffffff;
}
.page{
    display: flex;
    background-color: #E5E5E5;
}
.main {
  margin: 0;
  padding: 0;
  height: 100%;
  width: 100%;
  padding: 36px;
  /* background-color: red; */
}
.asider{
    width: 256px;
}
.col-head{
  display: flex;
  flex-direction: column;
  width: 100%;
}
@media screen and (max-width: 1279px ) and (min-width: 768px ){
.main {
  overflow-x: scroll;
  padding: 4%;
}
}
@media screen and (max-width: 767px){
.main {
  overflow-x: scroll;
  padding: 2%;
}
}
</style>
