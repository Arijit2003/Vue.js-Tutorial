
<template>
    <p v-bind:class="[firstStyle,mySecondStyle]">
      {{"Hello Mr." + myName }}
    </p>
</template>


<script setup>
  import { ref } from 'vue';
  const firstStyle = ref('firstStyle'); 
  const mySecondStyle = ref('secondStyle')
  const myName = ref('Arijit M.');

</script>


<style scoped>
  .firstStyle {
    color: red;
    text-decoration: underline;
    background-color: blue;
  }
  .secondStyle {
    background-color: blue;
  }

</style>
