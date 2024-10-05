<script setup>
</script>

<template>
    <div class="overall-container">
        <h1>Composant</h1>
        <p v-if="firstVar == 2">p n°111</p>
        <p v-else>p n°222222</p>
        <p> firstVar : {{ firstVar }}</p>
    </div>
</template>

<script>
export default {
  data() {
    return {
      firstVar: 1
    }
  }
}
</script>

<style scoped src="../assets/maincomp.css">
</style>