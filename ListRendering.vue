<script>
// выдаем всем todo уникальные id
let id = 0

export default {
  data() {
    return {
      newTodo: '',
      todos: [
        { id: id++, text: 'Изучить HTML' },
        { id: id++, text: 'Изучить JavaScript' },
        { id: id++, text: 'Изучить Vue' }
      ]
    }
  },
  methods: {
    addTodo() {
      // adding element 
      this.todos.push({ id: id++, text: this.newTodo })
      this.newTodo = ''
    },
    removeTodo(todo) {
      // removing element with callback function ('t' is array's element)
      this.todos = this.todos.filter((t) => t !== todo)
    }
  }
}
</script>

<template>
  <form @submit.prevent="addTodo">
    <input v-model="newTodo" required placeholder="new todo">
    <button>Добавить задачу</button>
  </form>
  <ul>
    <li v-for="todo in todos" :key="todo.id">
      {{ todo.text }}
      <button @click="removeTodo(todo)">X</button>
    </li>
  </ul>
</template>