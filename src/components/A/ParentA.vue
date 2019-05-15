<template>
  <div>
    <child-a v-model="value" />
    <small>parent: {{ value }} </small>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import ChildA from "@/components/A/ChildA.vue";

export default Vue.extend({
  components: { ChildA },
  data() {
    return {
      value: ""
    };
  }
});
</script>

<style scoped>
</style>