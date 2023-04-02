<template>
  <div @click="handleTodoItemClick($event)" :class="`${isDone ? 'done' : ''} box`">
    {{ item }}
    <button @click="handleTodoItemDelete()" class="button is-ghost has-text-danger">
      <nuxt-icon name="trash"></nuxt-icon>
    </button>
  </div>
</template>

<script setup>
defineProps({
  item: String,
  index: Number,
});
</script>

<script>
export default {
  data: () => ({
    isDone: false,
  }),
  emits: ['rewrite'],
  methods: {
    handleTodoItemClick() {
      this.isDone = !this.isDone;
    },
    handleTodoItemDelete() {
      this.$emit('todoDeleted', this.index)
    }
  }
};
</script>

<style scoped>
  div {
    user-select: none;
    display: flex;
    align-items: center;
  }

  .done {
    text-decoration: line-through;
  }
</style>