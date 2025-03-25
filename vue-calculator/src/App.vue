<script setup>
import { reactive, ref, computed } from "vue";
import number from "./number.vue";
import opSelect from "./opSelect.vue";
const e = reactive({
  num1: null,
  num2: null,
});
const select = reactive({ value: "" });

function soma() {
  return e.num1 + e.num2;
}
function sub() {
  return e.num1 - e.num2;
}
function mul() {
  return e.num1 * e.num2;
}
function div() {
  return e.num1 / e.num2;
}
const result = computed(() => {
  if (select.value === "") {
    return "Por favor, selecione uma operação.";
  }
  if (select.value === "sum") {
    return soma();
  }
  if (select.value === "sub") {
    return sub();
  }
  if (select.value === "mul") {
    return mul();
  }
  if (select.value === "div") {
    return div();
  }
});
</script>

<template>
  <div
    class="container flex flex-col bg-gray-200 mt-16 justify-center items-center h-100 m-auto gap-10 rounded-3xl"
  >
    <number :e="e" />
    <opSelect :select="select" :result="result" />
  </div>
</template>
