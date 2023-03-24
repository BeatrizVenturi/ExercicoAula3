<script setup>
import { ref, computed } from "vue";
const contador1 = ref(0)
const contador2 = ref(0)
const soma = computed(() => contador1.value + contador2.value)
const mostrar = ref(true)

</script>

<template>
  <button class="btn btn-danger" @click="mostrar = !mostrar"> Mostrar / Esconder</button>
  <div v-if="mostrar">
    <div>
      contador1: {{ contador1 }}
      <button class="btn btn-outline-primary" @click="contador1++"> + </button>
      <button class="btn btn-outline-primary" @click="contador1--">-</button>
    </div>
    <div>
      contador2: {{ contador2 }}
      <button class="btn btn-outline-primary" @click="contador2++"> + </button>
      <button class="btn btn-outline-primary" @click="contador2--">-</button>
    </div>
    <div>
      soma: {{ contador1 + contador2 }}
    </div>

    <div v-if="soma % 2 === 0">é par </div>

    <div v-else>impar</div>
  </div>
</template>

<style scoped></style>
