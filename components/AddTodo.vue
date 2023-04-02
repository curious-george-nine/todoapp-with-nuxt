<template>
  <input type="text" class="input mr-4 add-todo" placeholder="Add todo..."
    v-model="inputValue">
  <button class="button" @click="handleTodoSubmit()">add</button>
</template>

<script>
export default {
  data: () => ({
    inputValue: ""
  }),
  emits: ['rewrite'],
  methods: {
    handleTodoSubmit() {
      this.$emit("addTodo", this.inputValue);
    }
  }
}
</script>

<style scoped>
  .add-todo {
    max-width: 400px;
  }
</style>