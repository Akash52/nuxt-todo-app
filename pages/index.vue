<template>
  <div>
    <h1 class="text-4xl">Hello World</h1>
    <p>This is a simple example of a Vue.js component.</p>
    {{ couter }}
  </div>
</template>
<script>
import { mapState } from "vuex";
export default {
  computed: {
    ...mapState({
      counter: (state) => state.counter,
    }),
  },
};
</script>
