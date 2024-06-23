<script setup>
const props = defineProps(["name"]);
</script>

<template>
  <h1>DefineProps with composition api</h1>
  <div class="container-code">
    <code class="code">{{ name }}</code>
  </div>
</template>

<style>
.container-code {
  background-color: rgb(224, 224, 224);
  padding: 1em;
}

.code {
  font-size: 1.5em;
}
</style>
