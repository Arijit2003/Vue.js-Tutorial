
<template>
    <input type="text" ref = "txt1" /> </br>
    <button type = "button" @click = "show">Greet</button>
</template>


<script setup>
// local variable and template ref variable name should be same
  import { ref } from 'vue';
  const txt1 = ref('txt1');
  const show = () =>{
    // txt1  is a ref object, txt1.value refers to the input element
    alert(txt1.value.value);
  }

</script>


<style scoped>


</style>
