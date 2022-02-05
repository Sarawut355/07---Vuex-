
<template>
  <div class="hello">
    <h1>{{ getTodoById(id) }}</h1>
  </div>
</template>

<script>
import { mapGetters } from "vuex";
export default {
  name: "HelloWorld",
  props: {
    id:Number
  },
  computed: {
    // doneTodosCount() {
    //   return this.$store.getters.doneTodosCount
    // },
    ...mapGetters(["doneTodosCount", "doubleCounter", "getTodoById","doneTodos","getTodoById"]),
  },
};
</script>