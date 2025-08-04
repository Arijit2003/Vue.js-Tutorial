
<template>
    <input type="text" v-model = "myName" /> </br>
    <button type = "button" @click = "show">Greet</button>
    {{ myName }}
</template>


<script setup>

  import { ref } from 'vue';
  const myName = ref('Arijit Modak');
  const show = () =>{
    alert(txt1.value.value);
  }

</script>


<style scoped>


</style>
