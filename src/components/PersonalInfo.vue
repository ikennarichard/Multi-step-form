<script setup lang="ts">
import { reactive } from 'vue';
import FormInput from './FormInput.vue';

const model = reactive({
  username: '',
  email: '',
  phoneNumber: ''
})
</script>

<template>
  <h2>Personal Info</h2>
  <p>Please provide your name, email address, and phone number.</p>

  <div>
    <FormInput
      v-model="model.username"
      label="Name"
      id="username"
      name="username"
      placeholder="e.g. Stephen King"
    />
    <FormInput
      v-model="model.email"
      label="Email Address"
      id="email"
      name="email"
      type="email"
      placeholder="e.g. stephenking@lorem.com"
    />
    <FormInput
      v-model="model.phoneNumber"
      label="Phone Number"
      id="phone"
      name="phone"
      placeholder="e.g. +1234 567 890"
    />
  </div>
</template>

<style scoped>
</style>