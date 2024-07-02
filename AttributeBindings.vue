<script>
export default {
  data() {
    return {
      titleClass: 'title',
      rawHtml: "<span style='color: red'>Красный текст.</span>"
    }
  }
}
</script>

<template>
  <div :class='titleClass'>
    <h1>Сделай меня красным</h1> <!-- Добавьте сюда динамическую привязку класса -->
  </div>
  <p>Двойные фигурные скобки: {{ rawHtml }}</p>
  <p>Директива v-html: <span v-html="rawHtml"></span></p>
</template>

<style>
.title {
  color: red;
}
</style>