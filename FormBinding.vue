<script>
export default {
  data() {
    return {
      text: '',
      text1: ''
    }
  },
  methods: {
    onInput(e) {
      this.text = e.target.value
    }
  }
}
</script>

<template>
  <input :value="text" @input="onInput" placeholder="Пишите тут"> <!-- we can use v-bind and v-on together to change variable -->
  <p>{{ text }}</p>
  <input v-model="text1" placeholder="Так же, только круче"> <!-- same but shorter -->
	<p>{{ text1 }}</p>
</template>