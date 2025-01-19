<script setup lang="ts">
import FormButton from './components/FormButton.vue';
import PersonalInfo from './components/PersonalInfo.vue';
import StepCircle from './components/StepCircle.vue';

const handleSubmit = () => {
}

</script>

<template>
    <div class="wrapper">
      <div>
        <StepCircle />
      </div>
      <form @submit.prevent="handleSubmit">
        <PersonalInfo />
        <FormButton label="Next Step" type="submit" />
      </form>
    </div>
</template>

<style scoped>

</style>
