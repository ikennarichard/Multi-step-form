<script setup lang="ts">
import FormButton from './components/FormButton.vue';
import PersonalInfo from './components/PersonalInfo.vue';

const handleSubmit = () => {
  const formData = new FormData()
  console.log(formData)
}

</script>

<template>
    <div class="wrapper">

      <form @submit.prevent="handleSubmit">
        <PersonalInfo />
        <FormButton label="Next Step" type="submit" />
      </form>
    </div>
</template>

<style scoped>

</style>
