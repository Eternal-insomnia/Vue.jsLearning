<script>
export default {
  data() {
    return {
      message: 'Hello!',
      counter: {
        count: 0
      }
    }
  }
}
</script>

<template>
  <h1>Make me dynamic!</h1>
  <h1>{{message}}</h1> <!-- {{}} only for text interpolation (it's like changing key-word to something value) -->
  <p>Количество: {{counter.count}}</p>
  <p>{{message.split('').reverse().join('')}}</p>
</template>