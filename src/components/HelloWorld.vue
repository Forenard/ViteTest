<script setup>
import ClickCounter from "./ClickCounter.vue";
// import ItemList from "./ItemList.vue";
import TaskList from "./TaskList.vue";

defineProps({
  msg: { type: String, default: "" },
});
</script>

<template>
  <h1>{{ msg }}</h1>
  <ClickCounter />
  <TaskList />
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
