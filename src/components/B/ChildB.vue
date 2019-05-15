<template>
  <div>
    <grand-child-b :value="value" :input="input" />
    <small>child: {{ value }}</small>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import GrandChildB from "@/components/B/GrandChildB.vue";

export default Vue.extend({
  name: "child-b",
  components: { GrandChildB },
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

<style scoped>
</style>