<template>
  <div>Child component</div>
  <div>
    <button @click="props.decreamentCount(2)">-</button>
    <button @click="props.increamentCount(3)">+</button>
  </div>
</template>

<script setup>
import { defineProps } from "vue";
const props = defineProps(["increamentCount", "decreamentCount"]);
</script>

<style lang="scss" scoped></style>
