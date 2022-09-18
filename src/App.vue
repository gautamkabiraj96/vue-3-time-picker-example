<template>
  <div>
    <div class="time-preview">
      <div class="time-preview-time">
        {{ timeData.hh }}: {{ timeData.mm }}:
        {{ timeData.ss }}
        {{ timeData.a }}
      </div>
    </div>
    <vue-timepicker :format="timeFormat" v-model="timeData"></vue-timepicker>
  </div>
  <!--
    www.nightprogrammer.com
  -->
</template>

<script>
import VueTimePicker from "vue3-timepicker";
import "vue3-timepicker/dist/VueTimepicker.css";

export default {
  name: "App",
  data() {
    return {
      timeFormat: "hh:mm:ss a",
      timeData: {
        hh: "09",
        mm: "15",
        ss: "00",
        a: "am",
      },
    };
  },
  components: {
    "vue-timepicker": VueTimePicker,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #000000;
  margin-top: 60px;
}

.time-preview {
  border: 1px solid #eee;
  max-width: 400px;
  text-align: center;
  margin: 0 auto;
  margin-bottom: 20px;
  padding: 15px;
  background: rgb(70, 25, 173);
  color: #fff;
}

.time-preview-time {
  font-size: 30px;
}
</style>
