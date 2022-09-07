<template>
  <div class="wrapper">
    <ejs-daterangepicker placeholder="Select a date range"
      :startDate="startValue"
      :endDate="endValue"
      :min="minDate"
      format="dd-MMM-yy"
      start="Year"
      depth="Year"></ejs-daterangepicker>
      <!-- :max="maxDate" - To restrict end range
      :minDays="5" :maxDays="10" -> To restrict the minimum and maximum number of days selection in a range-->
  </div>
</template>

<script>
import {DateRangePickerComponent} from '@syncfusion/ej2-vue-calendars';

export default {
  name: 'App',
  components: {
    'ejs-daterangepicker': DateRangePickerComponent
  },
  data(){
    return{
      startValue: new Date("09/15/2022"),
      endValue: new Date("10/22/2022"),
      minDate: new Date("09/12/2022"),
      maxDate: new Date("10/26/2022")
    }
  }
}
</script>

<style>
  @import '../node_modules/@syncfusion/ej2-base/styles/material.css';
  @import '../node_modules/@syncfusion/ej2-buttons/styles/material.css';
  @import '../node_modules/@syncfusion/ej2-inputs/styles/material.css';
  @import '../node_modules/@syncfusion/ej2-popups/styles/material.css';
  @import '../node_modules/@syncfusion/ej2-lists/styles/material.css';
  @import "../node_modules/@syncfusion/ej2-vue-calendars/styles/material.css";
  .wrapper{
    max-width: 250px;
    margin: auto;
  }
</style>
