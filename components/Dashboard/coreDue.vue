<template>
  <div>
    <div class="duedate">
      <div>
        <h1>{{ setdata.do }}</h1>
        <div class="date">
          <p class="opa">
            Due date:
          </p>
          <p>December 23, 2018</p>
        </div>
        <p class="date-name">
          <img :src="setdata.image" alt="">
          {{ setdata.name }}
        </p>
      </div>
      <div class="status">
        <h2>{{ setdata.type }}</h2>
        <div class="list">
          <coreHover class="edit" />
          <coreButtonDash :status="setdata.status" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import coreButtonDash from '@/components/Button/coreButtonDash'
import coreHover from '@/components/Button/coreHover'
export default {
  components: {
    coreButtonDash,
    coreHover
  },
  props: {
    setdata: {
      type: Object,
      required: true
    }
  }

}
</script>
<style>
.duedate{
  background-color: #ffffff;
  display: flex;
  justify-content: space-between;
  padding: 16px;
  box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.08);
  border-radius: 4px;
  margin: 24px;
  cursor: pointer;
}
.date{
  display: flex;
}
h1{
  color: #323C47;
  font-weight: 500;
  font-size: 15px;
}
p{
  font-size: 13px;
  margin: 0 0 22px 0;
}
.date p{
  color: #4C5862;
}
.opa{
  opacity: 0.5;
}
.date-name{
  color: #707683;
  margin: 0 0 2px 0;
}
.date-name img{
  margin-right: 12px;
}
h2{
  font-size: 12px;
  color: #90A0B7;
  text-align: right;
}
.status{
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.list{
  display: flex;
}
.duedate:hover .edit{
  display: block;
}
.duedate:hover{
   box-shadow: 0px 0px 16px rgba(0, 0, 0, 0.14);
}
@media screen and (max-width: 1279px ) and (min-width: 768px ){

}
@media screen and (max-width: 767px){
.duedate{
  flex-direction: column;
}

}
</style>
