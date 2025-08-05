<template>
    <div>
      <h1>Employee List</h1>
        <table border="1">
            <thead>
            <tr>
                <th>Emp ID</th>
                <th>Emp Name</th>
                <th>Salary</th>
                <th>Department</th>
            </tr>
            </thead>
            <tbody>
            <tr v-for="employee in employees" :key="employee.empid">
                <td>{{ employee.empid }}</td>
                <td>{{ employee.empName }}</td>
                <td>{{ employee.salary }}</td>
                <td>{{ employee.deptName }}</td>
            </tr>
            </tbody>
        </table>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  // Define the fruits array as a reactive reference
  const employees = ref([
    {empid: 101, empName: 'Ajay', salary: 1000, deptName: 'HR'},
    {empid: 102, empName: 'Vijay', salary: 2000, deptName: 'Finance'},
    {empid: 103, empName: 'Ravi', salary: 3000, deptName: 'IT'},
    {empid: 104, empName: 'Sita', salary: 4000, deptName: 'Marketing'},
    {empid: 105, empName: 'Geeta', salary: 5000, deptName: 'Sales'},
  ]);
  </script>