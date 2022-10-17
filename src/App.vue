<script setup lang="ts">
import TodayDate from "./components/TodayDate.vue";
import ChronometerButtons from "./components/ChronometerButtons.vue";
import ChronometerSum from "./components/ChronometerSum.vue";
import ChronometerTable from "./components/ChronometerTable.vue";
import { useStopwatch } from 'vue-timer-hook';


const autoStart = true;
const stopwatch = useStopwatch(autoStart);
  
</script>

<template>
  <div class="container">
    <div class="row">
      <div class="col-6">
        <TodayDate />
      </div>

      <div class="col-6 flex flex-end">
        <ChronometerButtons :stopwatch="stopwatch"/>
        <ChronometerSum />
      </div>
    </div>

    <div class="row">
      <div class="col">
        <ChronometerTable :stopwatch="stopwatch"/>
      </div>
    </div>

    <div class="row">
      <div class="col sum-col">
        <div class="sum-text font-rb-25 dimgrey">Total</div>
        <ChronometerSum />
      </div>
    </div>
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}
.row {
  margin-bottom: 7%;
}
.flex {
  display: flex;
  align-items: center;
}
.flex-end {
  justify-content: center;
}
.sum-text {
  margin-right:22px
}
.sum-col{
  border-top: 1px solid #E8E8E8 ;
  border-bottom: 1px solid #E8E8E8 ;
  padding:14px;
  display: flex;
   justify-content: flex-end;
}
@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
