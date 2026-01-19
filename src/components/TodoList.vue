<template>
  <div class="todo-list-container">
    <h2>本周待办事项</h2>
    <ul class="todo-list">
      <TodoItem 
        v-for="item in todoList" 
        :key="item.id" 
        :item="item"
        @delete="$emit('delete', $event)"
      />
    </ul>
    <TodoInput @add="$emit('add', $event)" />
    <button class="clear-btn" @click="$emit('clear')">清空所有</button>
  </div>
</template>

<script>
import TodoItem from './TodoItem.vue'
import TodoInput from './TodoInput.vue'

export default {
  name: 'TodoList',
  components: {
    TodoItem,
    TodoInput
  },
  props: {
    todoList: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped>
.todo-list-container {
  width: 500px;
  margin: 60px auto;
  padding: 20px;
  background-color: #f5f5f5;
  border-radius: 8px;
  text-align: center;
}

h2 {
  color: #333;
  margin-bottom: 20px;
  font-size: 24px;
}

.todo-list {
  padding: 0;
  margin-bottom: 20px;
  list-style: none;
}

.clear-btn {
  background-color: #6c757d;
  color: #fff;
  border: none;
  padding: 10px 20px;
  border-radius: 4px;
  cursor: pointer;
  font-size: 14px;
}

.clear-btn:hover {
  background-color: #5a6268;
}
</style>