<template>
  <div id="app" class="container mt-5">
    <div class="row">
      <div class="col-12">
        <h1>input component sample</h1>
      </div>
    </div>
    <div class="row">
      <div class="col">
        <h2>emit pattern</h2>
        <parent-a />
      </div>
      <div class="col">
        <h2>props pattern</h2>
        <parent-b />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import ParentA from "@/components/A/ParentA.vue";
import ParentB from "@/components/B/ParentB.vue";

export default Vue.extend({
  name: "app",
  components: {
    ParentA,
    ParentB
  }
});
</script>

<style>
</style>
