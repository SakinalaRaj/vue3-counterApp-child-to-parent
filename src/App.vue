<template>
  <div id="app">
    <div>Parent Component count value: {{ count }}</div>
    <div>
      <ChildViewVue
        :increamentCount="increamentCount"
        :decreamentCount="decreamentCount"
      />
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import ChildViewVue from "./components/ChildView.vue";
const count = ref(0);
const decreamentCount = () => {
  count.value--;
};
const increamentCount = (a) => {
  console.log("a", a);
  count.value++;
};
</script>
<style>
#app {
  text-align: center;
  align-items: center;
}
</style>
