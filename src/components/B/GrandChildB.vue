<template>
  <div>
    <input type="text" class="input" :value="value" @input="input" />
    <small>grand child: {{ value }}</small>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "grand-child-b",
  props: {
    value: {
      type: String
    },
    input: {
      type: Function
    }
  }
});
</script>

<style  scoped>
</style>