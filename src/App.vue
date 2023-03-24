<script setup>
import { ref, computed } from "vue";
const contador1 = ref(0)
const contador2 = ref(0)
const soma = computed(() => contador1.value + contador2.value)


</script>

<template>
  <div>
    contador1: {{ contador1 }}
    <button @click="contador1++"> + </button>
    <button @click="contador1--">-</button>
  </div>
  <div>
    contador2: {{ contador2 }}
    <button @click="contador2++"> + </button>
    <button @click="contador2--">-</button>
  </div>
  <div>
    soma: {{ contador1 + contador2 }}
  </div>
  <div v-if="soma % 2 === 0">é par </div>
  <div v-else>impar</div>
</template>

<style scoped></style>
