<script>
import ChildComp from './ChildComp.vue';
export default {
    components: {
        ChildComp
    },
    data() {
        return {
            msg: "Какое-то сообщение от родителя"
        }
    }
}
</script>

<template>
    <ChildComp>{{ msg }}</ChildComp>
</template>