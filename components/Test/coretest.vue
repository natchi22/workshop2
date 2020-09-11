<template>
  <div class="frame">
    <p>{{ name }}</p>
    <p>สกุล</p>
    <p>อายุ</p>
  </div>
</template>

<style>
.frame{
  background-color: seagreen;
}
</style>
<script>
export default {
  props: {
    name: {
      type: String,
      required: true
    }
  }
}
</script>
