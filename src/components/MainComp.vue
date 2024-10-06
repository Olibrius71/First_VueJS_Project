<script>
import { ref } from 'vue'
</script>

<template>
    <div class="overall-container">
      <h1>Composant</h1>
      <div class="container information-container">
        <p v-if="firstVar == 1">Variable égale à 111</p>
        <p v-else-if="firstVar == 2">Variable égale à 222</p>
        <p v-else>Variable égale à autre valeur</p>
        <p> firstVar : {{ firstVar }}</p>
      </div>

      <div class="container list-container">
        <ul>
          <li v-for="item in liste">{{ item }}</li>
        </ul>
      </div>

      <div class="container buttons-container">
        <button @click="firstVar = 1">1</button>
        <button @click="changeVarValue(2)">2</button>
        <button @click="firstVar = 3">3</button>
        <button v-on:click="changeVarValue(10)">10</button>
      </div>

      <div class="container form-container">
        <form @submit.prevent="addElement($event)">
          <label for="newElementInput">Nouvel élément</label>
          <input type="text" id="newElementInput" name="newElement" v-model="newElement">
          <button type="submit">Ajouter</button>
        </form>
      </div>

    </div>
</template>

<script setup>
  const firstVar = ref(1);
  const liste = ref(["un", "deux", "trois", "quatre"]);
  const newElement = ref("");

  const changeVarValue = (value) => {
    firstVar.value = value
  }

  const addElement = (event) => {
    liste.value.push(newElement.value);
    newElement.value = "";
  }

</script>

<style scoped src="../assets/maincomp.css">
</style>