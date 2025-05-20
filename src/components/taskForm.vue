<script lang="ts" setup>
import { ref } from "vue";

const message = ref("Tasks App");
const newTask = ref("");

function formSubmitted() {
    console.log(newTask.value);
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