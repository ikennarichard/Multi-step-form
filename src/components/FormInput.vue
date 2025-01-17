<script setup lang="ts">
  const {type='text'} = defineProps<{
    label: string,
    placeholder: string,
    id: string,
    type?: string,
    name: string
  }>()

  const model = defineModel()
</script>

<template>
  <div>
    <label :for="id">{{label}}</label>
    <input :type="type" :placeholder="placeholder" v-model="model" :id="id" :name="name" required>
  </div>
</template>

<style scoped>

</style>