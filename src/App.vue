<script setup>
import DefinePropsA from "./components/DefinePropsA.vue";
import DefinePropsAValidation from "./components/DefinePropsAValidation.vue";
</script>

<template>
  <div>Learn vue 3</div>
  <h1>From the parent : {{ helloWorldComputed }}</h1>
  <DefinePropsA :name="'toto'" />
  <DefinePropsA :name="5" />
  <DefinePropsA :name="false" />
  <DefinePropsA
    :name="[
      'Hello world',
      1,
      false,
      {
        name: 'toto',
        disabled: false,
      },
    ]"
  />

  <hr />

  <DefinePropsAValidation :name="name" />
</template>

<style></style>
