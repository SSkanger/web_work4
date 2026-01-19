<template>
  <div class="input">
    <input 
      type="text" 
      v-model="newTodo" 
      placeholder="请输入待办事项..." 
      class="todo-input"
      @keyup.enter="addTodo"
    />
    <button class="add-btn" @click="addTodo">添加</button>
  </div>
</template>

<script>
export default {
  name: 'TodoInput',
  data() {
    return {
      newTodo: ''
    }
  },
  methods: {
    addTodo() {
      if (this.newTodo.trim() === '') {
        return
      }
      this.$emit('add', this.newTodo.trim())
      this.newTodo = ''
    }
  }
}
</script>

<style scoped>
.input {
  display: flex;
  margin-bottom: 20px;
}

.todo-input {
  flex: 1;
  padding: 10px;
  border: 1px solid #007bff;
  border-radius: 4px 0 0 4px;
  outline: none;
  font-size: 14px;
}

.todo-input:focus {
  border-color: #0056b3;
}

.add-btn {
  background-color: #007bff;
  color: #fff;
  border: none;
  padding: 10px 20px;
  border-radius: 0 4px 4px 0;
  cursor: pointer;
  font-size: 14px;
}

.add-btn:hover {
  background-color: #0056b3;
}
</style>