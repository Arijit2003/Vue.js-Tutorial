
<template>
    <input type="text" :value = "count" /> </br>
    <button type = "button" @click = "increment">+</button>
    <button type = "button" @click = "decrement">-</button>

</template>


<script setup>

  import { ref } from 'vue';
  
  const count = ref(0);
  
  const increment = () => {
    count.value ++;
  }
  const decrement = () => {
    count.value --;
  }

</script>


<style scoped>


</style>
