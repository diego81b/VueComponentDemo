<template>
  <form name="form-step">
    <h2 class="text-sm-center">{{ title }}</h2>
    <!-- <keep-alive> -->
    <!-- <component v-bind:is="stepName" :infrigment="infrigment" :nextStep="nextStep"></component> -->
    <step1 :infrigment="infrigment" :nextStep="nextStep"></step1>
    <step2 :infrigment="infrigment" :nextStep="nextStep"></step2>
    <!-- </keep-alive> -->
  </form>
</template>

<script>
import step1 from "./step1";
import step2 from "./step2";

export default {
  name: "stepComponent",
  components: {
    step1,
    step2
  },
  props: {
    title: String,
    infrigment: Object,
    stepName: String,
    nextStep: {
      type: Function
    }
  },
  data: () => ({}),
  computed: {},
  methods: {}
};
</script>
