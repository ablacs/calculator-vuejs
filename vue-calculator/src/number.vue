<script setup>
import { defineProps } from "vue";
const props = defineProps({
  e: Object,
});
</script>

<template>
  <div class="container flex justify-center items-center gap-10">
    <input
      v-model="props.e.num1"
      class="font-bold text-2xl focus:outline-none bg-white border-3 h-20 text-center rounded-3xl"
      type="number"
      placeholder="Primeiro número"
    />
    <input
      v-model="props.e.num2"
      class="font-bold text-center text-2xl focus:outline-none bg-white border-3 h-20 rounded-3xl"
      type="number"
      placeholder="Segundo número"
    />
  </div>
</template>
