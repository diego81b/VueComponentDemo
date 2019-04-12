<template>
  <form name="form1">
    <p>
      <input type="text" v-model="infrigment.year1" name="year2">
    </p>
    <p>
      <input type="text" v-model="infrigment.hour1" name="hour2">
    </p>
    <p>
      <button type="button" @click="nextStep('step2.vue')">Avanti</button>
    </p>
  </form>
</template>

<script>
export default {
  name: "step2",
  props: {
    infrigment: {
      type: Object
    },
    nextStep: {
      type: Function
    }
  },
  methods: {}
};
</script>