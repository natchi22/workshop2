<template>
  <div class="dashboard">
    <div class="totaldashboard">
      <coreDetailDashboard />
    </div>
    <div class="chart">
      <div class="line">
        <coreLine />
      </div>
      <div class="doughnut">
        <coreDoughnut />
      </div>
    </div>
  </div>
</template>

<script>
import coreDetailDashboard from '@/components/Dashboard/coreDetailDashboard'
import coreLine from '@/components/Chart/coreLine'
import coreDoughnut from '@/components/Chart/coreDoughnut'
export default {
  components: {
    coreDetailDashboard,
    coreLine,
    coreDoughnut
  }

}
</script>

<style>
.totaldashboard{
  background-color: #ffffff;
  box-shadow: 0px 6px 18px rgba(0, 0, 0, 0.06);
  border-radius: 4px;
  margin-right: 30px;
  width: 100%;
}
.dashboard{
  display: flex;
  background-color: #E5E5E5;
}
.line{
  background-color: #ffffff;
  box-shadow: 0px 6px 18px rgba(0, 0, 0, 0.06);
  border-radius: 4px;
  margin-bottom: 30px;
  width: 445px;
}
.doughnut{
  background-color: #ffffff;
  box-shadow: 0px 6px 18px rgba(0, 0, 0, 0.06);
  border-radius: 4px;
  width: 445px;

}
@media screen and (max-width: 1279px ) and (min-width: 768px ){
.dashboard{
  display: flex;
  flex-direction: column;
  /* min-width: 450px; */
  /* max-width: 450px; */
}
.totaldashboard{
  margin-bottom: 30px;
}
.line{
  width: 100%;
}
.doughnut{
  width: 100%;

}
}
@media screen and (max-width: 767px){
.dashboard{
  display: flex;
  flex-direction: column;
  /* min-width: 450px;
  max-width: 767px; */
}
.totaldashboard{
  margin-bottom: 30px;
  margin-right: 0;
}
.line{
  width: 100%;
}
.doughnut{
  width: 100%;
}
}
</style>
