<template>
  <div>
    <h1>VUE TODO WITH TYPESCRIPT</h1>
    <todo-input />
  </div>
</template>

<script lang="ts">
  import Vue from 'vue'
  import TodoInput from './components/TodoInput.vue'

  export default Vue.extend({
    components: { TodoInput },
    data() {
      return {
        todoText: '',
      }
    }
  })
</script>

<style scoped></style>