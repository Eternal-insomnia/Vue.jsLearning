<script>
export default {
  data() {
    return {
      awesome: true
    }
  },
  methods: {
    toggle() {
      this.awesome = !this.awesome // switches condition
    }
  }
}
</script>

<template>
  <!-- switching text with using directives v-if and v-else-->
  <button @click="toggle">Переключить</button>
  <h1 v-if="awesome">Vue - это потрясающе!</h1>
  <h1 v-else>О нет 😢</h1>
</template>