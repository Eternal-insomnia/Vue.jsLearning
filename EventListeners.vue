<script>
export default {
  data() { // some reactive data
    return {
      count: 0
    }
  },
  methods: { // like functions but methods
    increment() {
      this.count++; // to access 'data' variables use this.
    }
  }
}
</script>

<template>
  <!-- сделайте так, чтобы кнопка работала -->
  <button v-on:click="increment">Количество: {{ count }}</button>
</template>