<template>
  <div id="app" class="container p-5">
    <div class="row">
      <div class="col">
        <parent-a />
      </div>
      <div class="col">hi</div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import ParentA from "@/components/A/ParentA.vue";

export default Vue.extend({
  name: "app",
  components: {
    ParentA
  }
});
</script>

<style>
</style>
