<script setup>
import { ref } from "vue";
const tasks = ref([
  { name: "掃除", isDone: false },
  { name: "宿題", isDone: false },
]);
const newTaskName = ref("");

const addTask = () => {
  tasks.value.push({ name: newTaskName.value, isDone: false });
};
</script>

<template>
  <div>未完タスク一覧</div>
  <div v-for="task in tasks" :key="task.name">
    <div v-if="!task.isDone" class="task">
      <div class="name">{{ task.name }}</div>
      <button @click="task.isDone = true">完了</button>
    </div>
  </div>
  <div>完了タスク一覧</div>
  <div v-for="task in tasks" :key="task.name">
    <div v-if="task.isDone" class="task">
      <div class="name">{{ task.name }}</div>
    </div>
  </div>
  <div>
    <label>
      タスク名
      <input v-model="newTaskName" type="text" />
    </label>
    <button @click="addTask">add</button>
  </div>
</template>

<style></style>
