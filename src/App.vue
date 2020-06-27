<template>
  <div id="app">
    
    <datePicker />
  </div>
</template>

<script>
import datePicker from './components/datePicker.vue'

export default {
  name: 'App',
  components: {
    datePicker
  }
}
var state = {
  date: new Date(2020, 6,  16)
}
</script>

<style lang="scss">
*{
  margin: 0px;
  padding: 0px;
  font-family: sans-serif;
}
  #app{
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
    background: #f1f1f1;
  }
  $borderRadius: 20px;
  $borderRadiusShadow: 16px;
  $colorPrimary: #455AF7;
  .card {
    display: flex;
    flex-direction: column;
    overflow: hidden;
    width: 300px;
    height: 400px;
    border-radius: $borderRadius;
    box-shadow: 0 24px 38px 3px rgba(0, 0, 0, 0.025),
      0 9px 46px 8px rgba(0, 0, 0, 0.025), 0 11px 15px -7px rgba(0, 0, 0, 0.025);
  }
  .card-footer {
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-end;
    padding: 0 0 1rem;
    color: #666;
    background: #F5F6FA;
  }
  .card-footer__icon {
    font-size: 29px;
    margin-bottom: 0.5rem;
  }
  .card-footer__text {
    font-weight: 700;
    font-size: 0.875rem;
    color: #666;
  }
  .fab-button {
    position: absolute;
    right: 20px;
    bottom: -20px;
    width: 44px;
    height: 44px;
    border-radius: 50%;
    border: 0;
    background: $colorPrimary;
    color: white;
    font-family: 'Material Icons';
  }
  @mixin shadow-defaults {
    content: "";
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    background: rgba(255, 255, 255, 0.25);
  }
  .datepicker-wrapper {
    position: relative;
    z-index: 2;
    padding: 1rem;
    border-radius: $borderRadius;
    background: #fff;
    box-shadow: 0 24px 38px 3px rgba(0, 0, 0, 0.025);
    transform: translateY($borderRadius);
    margin-top: -$borderRadius;
    .vdp-datepicker__calendar {
      background: inherit;
      width: 100%;
      border: 0;
      font-size: 0.875rem;
      color: rgba(#090c22, 0.85);
    }
    .vdp-datepicker__calendar header span {
      font-weight: 700;
    }
    .vdp-datepicker__calendar .cell:not(.month):not(.year) {
      line-height: 38px;
      height: 38px;
      border-radius: 35%;
    }
    .vdp-datepicker__calendar .cell:not(.blank):not(.disabled).month:hover {
      border-color: $colorPrimary;
    }
    .vdp-datepicker__calendar .cell.selected,
    .vdp-datepicker__calendar .cell.selected:hover {
      background: $colorPrimary;
      color: white;
    }
    .vdp-datepicker__calendar .cell:not(.blank):not(.disabled).day:hover {
      background: #d9ddeb;
      border: 0;
    }
    .vdp-datepicker__calendar header .prev:after {
      border-right-color: $colorPrimary;
      font-family: 'Material Icons';
    }
    .vdp-datepicker__calendar header .next:after {
      border-left-color: $colorPrimary;
      font-family: 'Material Icons';
    }
    .vdp-datepicker__calendar .cell.day-header {
      opacity: 0.57;
    }
  }

</style>
