<script>
import ChildComp from './ChildComp.vue'; // importing the component
export default {
    components: {
        ChildComp // registrating the component
    },
    data () {
        return {
            childMsg: "Ничего, совсем ничего..."
        }
    }
}
</script>

<template>
    <!-- using the v-on directive, we listen for the event of the child component -->
    <ChildComp @response="(msg) => childMsg = msg"/> <!-- getting an additional argument -->
    <p>{{ childMsg }}</p>
</template>