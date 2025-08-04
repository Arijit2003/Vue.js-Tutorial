
<template>
    <p v-bind:style="myStyles">
      {{"Hello Mr." + myName }}
    </p>
</template>


<script setup>
  import { ref } from 'vue';
  const myStyles = ref({
    backgroundColor: 'blue',
    color: 'red',
    fontSize: '42px'
  }); 
  const myName = ref('Arijit M.');

</script>


<style scoped>


</style>
