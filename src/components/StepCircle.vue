<script setup lang="ts">

</script>

<template>
  <div class="container">
    <span>1</span>
    <span>2</span>
    <span>3</span>
    <span>4</span>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  gap: 10px;
  background-color: blue;
}

span {
  width: 40px;
  height: 40px;
  border-radius: 100%;
  border: 2px solid white;
  font-weight: 600;
  display: grid;
  place-content: center;
  color: white;
}
</style>