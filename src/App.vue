<script lang="ts" setup>
import { ref } from "vue";
import taskForm from "./components/taskForm.vue";

const message = ref("Tasks App");
</script>

<template>
  <main>
    <h1>{{ message }}</h1>
    <taskForm/>
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