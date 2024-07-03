<script>
let id = 0

export default {
  data() {
    return {
      newTodo: '',
      hideCompleted: false,
      todos: [
        { id: id++, text: 'Изучить HTML', done: true },
        { id: id++, text: 'Изучить JavaScript', done: true },
        { id: id++, text: 'Изучить Vue', done: false }
      ]
    }
  },
  computed: { // component option
    filteredTodos() { // computed property
      return this.hideCompleted
        ? this.todos.filter((t) => !t.done)
        : this.todos
    }
  },
  methods: {
    addTodo() {
      this.todos.push({ id: id++, text: this.newTodo, done: false })
      this.newTodo = ''
    },
    removeTodo(todo) {
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
    <li v-for="todo in filteredTodos" :key="todo.id"> <!-- using filteredTodos (computed property) instead todos (property) -->
      <input type="checkbox" v-model="todo.done">
      <span :class="{ done: todo.done }">{{ todo.text }}</span>
      <button @click="removeTodo(todo)">X</button>
    </li>
  </ul>
  <button @click="hideCompleted = !hideCompleted">
    {{ hideCompleted ? 'Показать все' : 'Скрыть выполненные' }}
  </button>
</template>

<style>
.done {
  text-decoration: line-through;
}
</style>