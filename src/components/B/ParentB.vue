<template>
  <div>
    <child-b :value="value" :input="handleInput" />
    <small>parent: {{ value }}</small>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import ChildB from "@/components/B/ChildB.vue";

export default Vue.extend({
  name: "parent-b",
  components: { ChildB },
  data() {
    return {
      value: ""
    };
  },
  methods: {
    handleInput(event: Event) {
      this.value = (event.currentTarget as HTMLInputElement).value;
    }
  }
});
</script>

<style scoped>
</style>