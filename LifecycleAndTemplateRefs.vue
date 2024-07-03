<script>
export default {
  mounted() { // using his hook to get access to an element
    this.$refs.pElementRef.textContent = "balls.ыые"
  }
}
</script>

<template>
  <p ref="pElementRef">Привет</p> <!-- template ref (reference to an element) -->
</template>