<template>
  <div class="container">
    <add-todo @add-todo="todos.push($event)" />
    <todo-item v-for="(todo, index) in todos" :item="todo" :index="index"
      @todo-deleted="todos = todos.filter((_, index) => $event != index)" />
  </div>
</template>

<script setup>
import AddTodo from "@/components/AddTodo.vue";
import TodoItem from "@/components/TodoItem.vue";
</script>

<script>
export default {
  data: () => ({
    todos: [],
  }),
};
</script>