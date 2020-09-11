<template>
  <div class="date">
    <a-tabs
      tab-position="bottom"
      class="tab-custom"
      @change="callback"
    >
      <a-tab-pane v-for="item in items" :key="item.key">
        <p slot="tab" class="show-day">
          {{ item.dayshort }}
        </p>
        <p slot="tab" class="show-date">
          {{ item.date }}
        </p>
        {{ item.date +' December, '+ item.day }}
      </a-tab-pane>
    </a-tabs>
  </div>
</template>
<script>

export default {
  data () {
    return {
      items: [
        {
          key: 1,
          date: 23,
          day: 'Sunday',
          dayshort: 'Sun'
        },
        {
          key: 2,
          date: 24,
          day: 'Monday',
          dayshort: 'Mon'
        },
        {
          key: 3,
          date: 25,
          day: 'Tuesday',
          dayshort: 'Tue'
        },
        {
          key: 4,
          date: 26,
          day: 'Wednesday',
          dayshort: 'Wed'
        },
        {
          key: 5,
          date: 27,
          day: 'Thursday',
          dayshort: 'Thu'
        },
        {
          key: 6,
          date: 28,
          day: 'Friday',
          dayshort: 'Fri'
        },
        {
          key: 7,
          date: 29,
          day: 'Saturday',
          dayshort: 'Sat'
        }
      ]
    }
  },
  methods: {
    callback (key) {
      console.log(key)
    }
  }
}
</script>
<style scoped>
.date{
    background-color: #ffffff;
    border-bottom: 1px solid #EBEFF2;
}
.show-day{
    color: rgba(51, 77, 110,0.5);
}
.show-date{
    color: #4C5862;
}
.tab-custom .ant-tabs-tab:hover .show-date,
.tab-custom .ant-tabs-tab:hover .show-day{
    color: #109CF1;
}
.tab-custom .ant-tabs-tab-active .show-date{
    color: #ffffff;
}
.tab-custom .ant-tabs-tab-active .show-day{
    color: #109CF1;
}
.tab-custom .ant-tabs-tab-active:hover .show-date{
    color: #ffffff;
}

</style>
<style>
.tab-custom .ant-tabs{
    padding: 0 24px;
}
.tab-custom .ant-tabs-ink-bar{
    background-color: #109CF1 !important;
    border-radius: 50px;
    height: 24px;
    width: 24px !important;
    z-index: 0;
    color: #fff;
}
.ant-tabs-bottom .ant-tabs-bottom-bar{
    border-top: none;
}
.tab-custom .a-tab-pane p{
    font-weight: 500;
    font-size: 15px;
    line-height: 22px;
    color: #192A3E;
}
.tab-custom .ant-tabs-nav .ant-tabs-tab-active{
    z-index: 1;
}
.tab-custom .ant-tabs-nav .ant-tabs-tab{
    width: 32px;
    /* width: 100%; */
    min-width: 14px;
    max-width: 40px;
    text-align: center;
    padding: 12px 0;
    /* margin: 0 92px 0 0; */
}
.ant-tabs-bottom .ant-tabs-bottom-bar .ant-tabs-ink-bar{
    top: 51px ;
    left: 4px;
}
.ant-tabs{
    padding: 0 24px;
    margin-top: 14px;
}
.ant-tabs .ant-tabs-bottom-content > .ant-tabs-tabpane{
    color: #192A3E;
    font-weight: 500;
    font-size: 15px;
    line-height: 22px;
}

</style>
