<script setup>
import { computed, ref } from "vue";

const nums = ref([1, 2, 3, 4, 5, 6]);
const counter  = ref(0);

const numberEven = computed(() => {

    console.warn("ALERT !!! numberEven method is called")
    return nums.value.filter((i) => i % 2 === 0);
})

function increment(){
    counter.value++;
}
</script>

<template>
  <h1>What is the computed ?</h1>
  <p>This is just a function who return a value no MUTATE</p>
  <p>Example :</p>

  <code> [1,2,3,4,5,6]</code>
  <p>I need to get the even number</p>
  <p>
    Result with a simple function like this
    <br />
    <code
      >function numberEven() { return nums.value.filter((i) => i % 2 === 0); }
    </code>
    <br />
    <p>It works correctly , look : : {{ numberEven }}</p>
    <p>But when i update another reactive variable like the counter, look your browser console</p>

    <h1>Counter : {{ counter }} </h1>
    <button @click="increment()"> Increment </button>
    <p>Now look your console</p>

    <p>For avoid this behavior, you can make transform the function component to a computed like this </p>
    <code>const numberEven = computed(() => nums.value.filter((i) => i % 2 === 0))</code>

  </p>
</template>
