
<template>

  <table border="1">
    <tbody>

    <tr>
      <th>First Number</th>
      <td> <input type="text" ref="fnum"/></td>
    </tr>

    <tr>
      <th>Second Number</th>
      <td> <input type="text" ref="snum"/></td>
    </tr>


    <tr>
      <th>Results</th>
      <td> <input type="text" ref="res"/></td>
    </tr>

    <tr>
      <td><button type="button" @click="sum">Add</button></td>
      <td><button type="button" @click="sub">Sub</button></td>
    </tr>

    <tr>
      <td><button type="button" @click="mul">Mul</button></td>
      <td><button type="button" @click="div">Div</button></td>
    </tr>

  </tbody>

  </table>

</template>


<script setup>

  import { ref } from 'vue';
  

  const fnum = ref('fnum');
  const snum = ref('snum');
  const res = ref('res');

  const  sum = () => {
    res.value.value = parseFloat(fnum.value.value) + parseFloat(snum.value.value);
  }

  const  sub = () => {
    res.value.value = parseFloat(fnum.value.value) - parseFloat(snum.value.value);
  }

  const  mul = () => {
    res.value.value = parseFloat(fnum.value.value) * parseFloat(snum.value.value);
  }

  const  div = () => {
    res.value.value = parseFloat(fnum.value.value) / parseFloat(snum.value.value);
  }
  

</script>


<style scoped>

  table, th, td {
    border-collapse: collapse;
    border: 1px solid black;
  }

</style>
