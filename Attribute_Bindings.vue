<script setup>
import { ref } from 'vue'

const titleClass = ref('title')
const rawHtml = ref("<span style='color: red'>Красный текст.</span>")
</script>

<template>
  <div v-bind:class="titleClass"> <!-- All directives starts with v- -->
    <h1>Сделай меня красным</h1> <!-- Добавьте сюда динамическую привязку класса -->
  </div>
  <div :class="titleClass">
    <h1>Одно и то же, что выше</h1>
  </div>
  <!-- Example using v-html derective-->
  <p>Двойные фигурные скобки: {{ rawHtml }}</p>
  <p>Директива v-html: <span v-html="rawHtml"></span></p>
</template>

<style>
.title {
  color: red;
}
</style>