<template>
  <form name="form1">
    <p>
      <input type="text" v-model="infrigment.year1" name="year1">
    </p>
    <p>
      <input type="text" v-model="infrigment.hour1" name="hour1">
    </p>
    <p>
      <button type="button" @click="submitStep('step1.vue')">Avanti</button>
    </p>
  </form>
</template>

<script>
export default {
  name: "step1",
  props: {
    infrigment: {
      type: Object
    },
    nextStep: {
      type: Function
    }
  },
  methods: {
    submitStep(step) {
      // this.infrigment.year2 = this.infrigment.year1;
      // this.infrigment.hour2 = this.infrigment.hour1;
    }
  }
};
</script>
