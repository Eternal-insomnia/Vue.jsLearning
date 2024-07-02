<script setup>
import { ref } from 'vue'
import { reactive } from 'vue'

  const message = ref('ыые') // works with any value types
  message.value = 'Изменено' // needs .value
  
  const counter = reactive({ // only works on objects (including arrays and built-in types such as Map & Set)
    count: 0
  })
  counter.count++ // don't need .value
</script>

<template>
  <h1>Сделай меня динамическим!</h1>
  <h1>{{message}}</h1>
  <p>Количество: {{counter.count}}</p>
  <p>{{message.split('').reverse().join('')}}</p>
</template>