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
                <th>Action</th>
            </tr>
            </thead>
            <tbody>
            <tr v-for="(employee, index) in employees" :key="employee.empid">
                <td>{{ employee.empid }}</td>
                <td>{{ employee.empName }}</td>
                <td>{{ employee.salary }}</td>
                <td>{{ employee.deptName }}</td>
                <td> <button type="button" @click = "deleteEmployee(index)">Delete</button></td>
            </tr>
            </tbody>
        </table>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import { empList } from './employeedata';
  
  // Define the fruits array as a reactive reference
  // u
  const employees = ref(empList);

  const deleteEmployee = (index) => {
    // Remove the employee at the specified index
    const flag = confirm("Are you sure you want to delete this employee?");
    if(flag) employees.value.splice(index, 1);
  };
  </script>