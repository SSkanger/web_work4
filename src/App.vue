<template>
  <div id="app">
    <TodoList 
      :todo-list="todoList"
      @add="addTodo"
      @delete="deleteTodo"
      @clear="clearTodos"
    />
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue'

export default {
  name: 'App',
  components: {
    TodoList
  },
  data() {
    return {
      todoList: [
        { id: 1, text: '去图书馆学习' },
        { id: 2, text: '上羽毛球课' },
        { id: 3, text: '会议室开会' }
      ],
      nextId: 4
    }
  },
  methods: {
    addTodo(text) {
      this.todoList.push({ id: this.nextId, text })
      this.nextId++
    },
    deleteTodo(id) {
      this.todoList = this.todoList.filter(item => item.id !== id)
    },
    clearTodos() {
      this.todoList = []
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Arial', sans-serif;
  background-color: #f8f9fa;
  line-height: 1.6;
}

#app {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>