<template>
  <div id="app">
    <h1>TEST</h1>
    <!-- <div v-for="(step, i) in ['step1', 'step2']" :key="i">
      <step-component :infrigment="infrigment" :step-name="step" :title="step" :nextStep="nextStep"></step-component>
    </div>-->
    <step1 :infrigment="infrigment" :nextStep="nextStep"></step1>
    <step2 :infrigment="infrigment" :nextStep="nextStep"></step2>
  </div>
</template>

<script>
import StepComponent from "./components/step";
import Step1 from "./components/step1";
import Step2 from "./components/step2";

export default {
  name: "App",
  components: {
    StepComponent,
    Step1,
    Step2
  },
  data: () => ({
    infrigment: {
      year1: "y1",
      hour1: "h1",
      year2: "y2",
      hour2: "h2"
    }
  }),
  methods: {
    nextStep(step) {
      console.log(step);
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
