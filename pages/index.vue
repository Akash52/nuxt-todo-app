<template>
  <div class="flex justify-center mt-8">
    <button
      class="text-white text-lg font-bold bg-blue-700 px-4 py-2 rounded"
      @click="increment"
    >
      +
    </button>
    <h1 class="text-4xl mr-2 ml-2">
      {{ counter }}
    </h1>
    <button
      class="text-white text-lg font-bold bg-blue-700 px-4 py-2 rounded"
      @click="decrement"
    >
      -
    </button>
  </div>
</template>
<script>
import { mapState, mapMutations } from "vuex";
export default {
  computed: {
    ...mapState({
      counter: (state) => state.counter,
    }),
  },
  methods: {
    ...mapMutations(["increment", "decrement"]),
  },
};
</script>
