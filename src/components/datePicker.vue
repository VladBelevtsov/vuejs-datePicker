<template>
  <div class="card">
    <div class="datepicker-wrapper">
      <button class="fab-button material-icons-outlined">add</button>
      <Datepicker value mondayFirst inline></Datepicker>
    </div>
    <div class="card-footer">
      <span class="card-footer__icon material-icons">date_range</span>
      <div class="card-footer__text">
        No Events
      </div>
    </div>
  </div>
</template>

<script>
import Datepicker from "vuejs-datepicker";

export default {
  name: 'datePicker',
  components: { Datepicker },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
