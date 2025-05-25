<script lang="ts" setup>
import { ref } from "vue";

const emit = defineEmits<{
    addTask: [newTask: string]
}>();

const newTask = ref("");

function formSubmitted() {
    if (newTask.value.trim()) {
        emit("addTask", newTask.value);
        newTask.value = "";
    }
}
</script>

<template>
    <form @submit.prevent="formSubmitted">
        <label>
            New task
            <input v-model="newTask" type="text" name="new task">
        </label>
        <div class="button">
            <button>add</button>
        </div>
    </form>
</template>