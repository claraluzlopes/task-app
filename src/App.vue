<script lang="ts" setup>
import { ref } from "vue";
import taskForm from "./components/taskForm.vue";
import type { Task } from "./types";

const message = ref("Tasks App");
const tasks = ref<Task[]>([]);

function addTask(newTask: string) {
    tasks.value.push({
    id: crypto.randomUUID(),
    title: newTask,
    done: false,
    });
}
</script>

<template>
  <main>
    <h1>{{ message }}</h1>
    <taskForm @add-task="addTask"/>
    <h3>there are {{ tasks.length }} tasks.</h3>
  </main>
</template>

<style>
main{
  max-width: 500px;
  margin: 3rem auto;
}

.button {
  display: flex;
  justify-content: flex-end; 
}
</style>