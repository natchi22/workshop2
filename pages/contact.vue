<template>
  <section class="contact">
    <div class="cilck">
      <coreSelect />
      <coreButtonContact />
    </div>
    <coreContact />
  </section>
</template>

<script>
import coreContact from '@/components/Contacts/coreContact'
import coreButtonContact from '@/components/Button/coreButtonContact'
import coreSelect from '@/components/Contacts/coreSelect'
export default {
  components: {
    coreContact,
    coreButtonContact,
    coreSelect

  }

}
</script>

<style>
.contact{
  background: #ffffff;
  width: 100%;
  /* margin: 36px; */
}
.cilck{
  display: flex;
  width: 100%;
  justify-content: space-between;
  padding: 0 0 24px 0;
  background-color: #E5E5E5;
}
@media screen and (max-width: 1279px ) and (min-width: 768px ){
.contact{
  width: 1000px;
}
}
@media screen and (max-width: 767px){
.contact{
  width: 1000px;
}
}
</style>
