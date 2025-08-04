<script setup>
import { ref } from 'vue';

const myName = ref('Arijit M.');

</script>

<template>
    <input type = "text" v-bind:value = "myName" />
</template>

<style scoped>
  h1 {
    color: red;
    text-decoration: underline;
    background-color: blue;
  }

</style>
