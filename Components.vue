<script>
import ChildComp from './ChildComp.vue' // importing the component

export default {
  components: { // register the component
    ChildComp
  }
}
</script>

<template>
  <ChildComp /> <!-- using the component-->
</template>