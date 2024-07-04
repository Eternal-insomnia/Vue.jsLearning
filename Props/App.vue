<script>
import ChildComp from './ChildComp.vue' // import component

export default {
  components: {
    ChildComp // registrating component
  },
  data() {
    return {
      greeting: 'Привет от родителя'
    }
  }
}
</script>

<template>
  <ChildComp :msg="greeting" /> <!-- giving property to msg -->
</template>