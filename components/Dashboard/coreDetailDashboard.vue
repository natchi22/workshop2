<template>
  <div class="total">
    <coreProgress />
    <coreDate />
    <coreDue
      v-for="item in due"
      :key="item.id"
      :setdata="item"
    />
    <coreHover />
    <h6>Show more</h6>
  </div>
</template>

<script>
import coreProgress from '@/components/Dashboard/coreProgress'
import coreDate from '@/components/Dashboard/coreDate'
import coreDue from '@/components/Dashboard/coreDue'
import coreHover from '@/components/Button/coreHover'
export default {
  components: {
    coreProgress,
    coreDate,
    coreDue,
    coreHover
  },

  data () {
    return {
      due: [
        {
          id: 1,
          do: 'Send benefit review by Sunday',
          image: require('~/assets/images/layout/03.png'),
          name: 'George Fields',
          type: 'Reminder',
          status: 'Completed'
        },
        {
          id: 2,
          do: 'Invite to office meet-up',
          image: require('~/assets/images/layout/04.png'),
          name: 'Rebecca Moore',
          type: 'Call',
          status: 'Ended'
        },
        {
          id: 3,
          do: 'Office meet-up',
          image: require('~/assets/images/layout/01.png'),
          name: 'Lindsey Stroud',
          type: 'Event',
          status: 'Completed'
        }
      ]
    }
  }
}
</script>

<style>
.dashboard{
  background: #ffffff;
  width: 100%;
}
.total{
  padding: 10px 0 14px 0;
}
.total h6{
  color: #109CF1;
  font-weight: 600;
  font-size: 13px;
  text-align: center;
}
</style>
