<script setup lang="ts">
const month = ["Jan","Feb","Mar","Apr","May","June","July","Aug","Sep","Oct","Nov","Dec"];
const d = new Date();
let  monthName = month[d.getMonth()];
let day = d.getDate();

</script>

<template>
  <div class="today-date">
    <h1 class="bleu font-rb-30">Today, {{day}} {{ monthName }}</h1>
  </div>
</template>

<style scoped>

</style>
