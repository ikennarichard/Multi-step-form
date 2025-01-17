<script setup lang="ts">
import { ref } from 'vue'
defineProps<{
  msg: string
}>()

const status = ref(true)
const home = 'essentials.com'
const newTask = ref('')
const tasks = ref(['First, task'])

const toggleStatus = () => {
  if (status.value) {
    status.value = false
  }
}

const addTask = () => {
  if (newTask.value.trim() != '') {
    tasks.value.push(newTask.value)
  }
  return
}
</script>

<template>
  <h1 v-if="status">Hello Vue</h1>
  <a :href="home">Click me</a>
  <button @click="toggleStatus">Change link</button>

  <!-- form -->
  <form @submit.prevent="addTask">
    <label for="new-task">New Task</label>
    <input type="text" v-model="newTask" id="new-task" />
    <button>Add task</button>
  </form>

  <ul>
    <li v-for="(task, index) in tasks" :key="index">
      {{ task }}
    </li>
  </ul>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
