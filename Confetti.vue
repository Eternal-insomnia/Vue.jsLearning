<script>
import JSConfetti from 'js-confetti'
const confetti = new JSConfetti()

export default {
    mounted() {
        this.showConfetti()
    },
    methods: {
        showConfetti() {
            confetti.addConfetti()
        }
    }
}
</script>

<template>
    <h1 @click="showConfetti">🎉 Поздравляем!</h1>
</template>