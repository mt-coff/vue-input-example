<template>
  <div>
    <grand-child :value="value" @input="handleInput" />
    <small> child: {{ value }} </small>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import GrandChild from "@/components/A/GrandChildA.vue";

export default Vue.extend({
  name: "child-a",
  components: { GrandChild },
  props: {
    value: {
      type: String
    }
  },
  methods: {
    handleInput(value: string) {
      this.$emit("input", value);
    }
  }
});
</script>

<style scoped>
</style>