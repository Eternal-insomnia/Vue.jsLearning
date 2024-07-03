<script>
export default {
  data() {
    return {
      todoId: 1,
      todoData: null
    }
  },
  methods: {
    async fetchData() {
      this.todoData = null
      const res = await fetch(
        `https://jsonplaceholder.typicode.com/todos/${this.todoId}`
      )
      this.todoData = await res.json()
    }
  },
  mounted() {
    this.fetchData()
  },
  watch: { // another component option
    todoData() { // if we see that todoData has changed, then we perform side effect
      this.fetchData()
    }
  }
}
</script>

<template>
  <p>Id задачи: {{ todoId }}</p>
  <button @click="todoId++" :disabled="!todoData">Получение следующего задания</button>
  <p v-if="!todoData">Загрузка...</p>
  <pre v-else>{{ todoData }}</pre>
</template>