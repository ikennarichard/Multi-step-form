<script setup lang="ts">
  const {type = 'button'} = defineProps<{
    label: string,
    type?: "button" | "submit" | "reset" | undefined,
  }>()
  defineEmits(['handleClick'])
// const openReadmeInEditor = () => fetch('/__open-in-editor?file=README.md')
</script>

<template>
  <button @click="$emit('handleClick')" :type="type">{{label}}</button>
</template>
