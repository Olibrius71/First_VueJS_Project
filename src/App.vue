<script setup>
import HelloWorld from './components/HelloWorld.vue'
import MainComp from './components/MainComp.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="90" height="90" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </header>

  <main>
    <MainComp />
  </main>
</template>

<style>
.logo {
  display: block;
  margin: 0 auto;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
