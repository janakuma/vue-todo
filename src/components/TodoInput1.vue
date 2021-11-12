<template>
  <div>
    <label for="todo-input">오늘 할 일 : </label>
    <input id="todo-input" type="text" :value="item" @input="handleInput" />
    <button @click="addTodo">add</button>
    <button @click="testTodo">testTodo</button>
  </div>
</template>
<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  props: {
    item: { type: String, default: "" },
  },
  methods: {
    handleInput(event: any) {
      this.$emit("input", event.target.value);
    },
    addTodo() {
      this.$emit("add");
    },
    testTodo() {
      this.$emit("test");
    },
  },
});
</script>

<style scoped></style>
