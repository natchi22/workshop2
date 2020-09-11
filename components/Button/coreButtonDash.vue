<template>
  <div>
    <button v-if="status === 'Completed'" class="btn color-green">
      Completed
    </button>
    <button v-if="status === 'Ended'" class="btn color-red">
      Ended
    </button>
    <button v-if="status === 'Active'" class="btn color-orenge">
      Active
    </button>
  </div>
</template>
<style>
.btn{
  width: 84px;
  color: #FFFFFF;
  font-weight: 500;
  font-size: 11px;
  line-height: 16px;
  border-radius: 4px;
  border: none;
  cursor: pointer;
  outline: none;
}
.color-green{
  background: #2ED47A;
}
.color-red{
  background: #F7685B;
}
.color-orenge{
  background: #FFB946;
}
</style>
<script>
export default {
  props: {
    status: {
      type: String,
      required: true
    }
  }
}
</script>
