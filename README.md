# vue-input-example

This repo is sample.

## Emit pattern

`v-model` is available.

```html
<template>
  <input type="text" :value="value" @input="handleInput" />
</template>

<script>
  import Vue from "vue";

  export default Vue.extend({
    props: {
      value: {
        type: String
      }
    },
    methods: {
      handleInput(event) {
        this.$emit("input", event.currentTarget.value);
      }
    }
  });
</script>
```

## Props pattern

`v-model` is not available.

```html
<template>
  <input type="text" class="input" :value="value" @input="input" />
</template>

<script>
  import Vue from "vue";

  export default Vue.extend({
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
```
