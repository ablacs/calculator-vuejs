<script setup>
import { defineProps } from "vue";
const props = defineProps({ select: Object, result: Object });
</script>

<template>
  <div class="container flex justify-center items-center flex-col gap-10">
    <select
      v-model="props.select.value"
      class="bg-white border-3 rounded-3xl p-3 font-bold"
    >
      <option value="">Selecione uma operação</option>
      <option value="sum">Soma</option>
      <option value="sub">Subtração</option>
      <option value="mul">Multiplicação</option>
      <option value="div">Divisão</option>
    </select>
    <p class="text-2xl font-bold">Resultado : {{ props.result }}</p>
  </div>
</template>
