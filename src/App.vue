<script setup>
import { RouterLink, RouterView } from 'vue-router'
import ToDoList from './components/ToDoList.vue'
import { ref } from 'vue'

const todos = ref([
  { title: 'Lorean Ipsum1', isDone: false },
  { title: 'Lorean Ipsum2', isDone: false },
  { title: 'Lorean Ipsum3', isDone: false },
])

const markTodoAsComplete = (index) => {
  todos.value[index].isDone = !todos.value[index].isDone
}
const createTodoHandler = () => {
  const todoTitle = prompt('Enter todo title')

  todos.value.push({
    title: todoTitle,
    isDone: false,
  })
}

const deleteTodoHandler = (index) => {
  todos.value.splice(index, 1)
}
</script>

<template>
  <div id="todo-page">
    <div id="todo">
      <header>GGIT ToDo</header>

      <ToDoList
        :todos="todos"
        @complete-todo="markTodoAsComplete"
        @delete-todo="deleteTodoHandler"
      />

      <button @click="createTodoHandler">+ New Task</button>
    </div>
  </div>
</template>

<style scoped>
header {
  background-color: blueviolet;
  color: aliceblue;
  padding: 24px;
  font-weight: 600;
}

#todo {
  width: 100%;
  max-width: 250px;
}
#todo-page {
  min-height: 100vh;
  min-width: 100vw;
  overflow: hidden;

  display: flex;
  align-items: center;
  justify-content: center;

  background-color: aliceblue;
}
#todos-container {
  background-color: white;
  padding: 24px;
  margin-top: 24px;
}
button {
  color: white;
  background-color: blue;
  padding: 12px 16px;
  font-size: 18 px;
  border: none;
  border-radius: 50px;
  margin: auto;
  margin-top: -22px;
  display: block;
}
</style>
