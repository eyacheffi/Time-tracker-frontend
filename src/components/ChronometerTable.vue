<script >
// import axios from 'axios';
//  const  getData = async () =>{
//        await axios.get("localhost:3333/timer").then(response => {console.log(response.data);})

// }
 
//  getData()
// export default {
//   data() {
//     return {
//       time: '00:00:00'
//   }
//     }
//   }
// export default {
//   name: 'StopWatch',
//   props:['stopwatch'],
//    components:{
 

//   }
// }
import { defineComponent } from 'vue';
export default defineComponent({
 props: {
   stopwatch: Object,
  },
})
</script>

<template>

  <div class="row row-chrono-table active">
    <div class="col-8">
      <div class="periode-name grey font-rb-16">Period 1</div>
    </div>

    <div class="col-2">
      <div class="slategrey font-rb-14">10:45 - 12:09 pm</div>
    </div>

    <div class="col-2">
      <div class="bleu font-rl-25"><span class="font-rb-25">{{stopwatch.hours}}:{{stopwatch.minutes}}</span>:<span>{{stopwatch.seconds}}</span></div>
    </div>
  </div>

  <div class="row row-chrono-table">
    <div class="col-8">
      <div class="grey font-rb-16">Period 1</div>
    </div>

    <div class="col-2">
      <div class="slategrey font-rb-14">10:45 - 12:09 pm</div>
    </div>

    <div class="col-2">
      <div class="bleu font-rm-25">1:23:51</div>
    </div>
  </div>

  <div class="row row-chrono-table">
    <div class="col-8">
      <div class="grey font-rb-16">Period 1</div>
    </div>

    <div class="col-2">
      <div class="slategrey font-rb-14">10:45 - 12:09 pm</div>
    </div>

    <div class="col-2">
      <div class="bleu font-rm-25">1:23:51</div>
    </div>
  </div>
</template>

<style scoped>
.row-chrono-table {
  border-top: 1px solid #e8e8e8;
  padding: 27px;
  align-items: center;
}
.row-chrono-table.active {
  border-color: #60b669;
  border-bottom: 1px solid #60b669;
}
.active .bleu {
  color: #60b669 !important;
}
</style>
