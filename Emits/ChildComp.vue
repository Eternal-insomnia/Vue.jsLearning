<script>
export default {
    // announcement of generated events
    emits: ['response'],
    created() {
        // generating event with parameters (1st - name, 2nd and another - additional)
        this.$emit('response', 'саламчик от дочернего компонента')
    }
}
</script>

<template>
    <p>Дочерний компонент</p>
</template>