<script>
export default {
  props: {
    msg: String // prop
  }
}
</script>

<template>
  <h2>{{ msg || 'пока входные параметры не переданы' }}</h2> <!-- this is displayed on the page -->
</template>