<script setup>
defineProps({
  name: String,
  price: Number,
});
</script>

<template>
  <h1>Define a props with validation</h1>
  {{ name }}
  <p>Check your browser console</p>
</template>
