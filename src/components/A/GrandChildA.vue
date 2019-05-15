<template>
  <div>
    <input type="text" :value="value" @input="handleInput" class="input" />
    <small>grand child: {{ value }}</small>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "grand-child-a",
  props: {
    value: {
      type: String
    }
  },
  methods: {
    handleInput(event: Event) {
      this.$emit("input", (event.currentTarget as HTMLInputElement).value);
    }
  }
});
</script>

<style scoped>
</style>