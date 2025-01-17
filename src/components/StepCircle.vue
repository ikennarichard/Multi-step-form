<script setup lang="ts">
import { ref } from 'vue'

defineProps<{
  step: number;
}>()


</script>

<template>
  <h1 v-if="status">Hello Vue</h1>
  <a :href="home">Click me</a>
  <button @click="toggleStatus">Change link</button>

  <!-- form -->
  <form @submit.prevent="addTask">
   
  </form>

  <ul>
    <li v-for="(task, index) in tasks" :key="index">
      {{ task }}
    </li>
  </ul>
</template>