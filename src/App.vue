<script setup>
import { ref } from 'vue';

  const num1 = ref(0);
  const num2 = ref(0);
  const number = ref(0);

  let suma = () => {
    number.value = num1.value + num2.value;
  }

  let resta = () => {
    number.value = num1.value - num2.value;
  }

  let multiplicación = () => {
    number.value = num1.value * num2.value;
  }

  let división = () => {
    number.value = num1.value / num2.value;
  }
</script>

<template>
  <h1>Calculadora</h1>
  <input type="number" v-model="num1">
  <input type="number" v-model="num2">
  <br>
  <button @click="suma">+</button>
  <button @click="resta">-</button>
  <button @click="multiplicación">*</button>
  <button @click="división">/</button>
  <p>Resultado: {{ number }}</p>
</template>

<style>
  h1{
    color: rgb(255, 148, 201);
  }
</style>