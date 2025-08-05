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
                <EmployeeComponent v-for="e in employees" :emp="e" @deleteEmp = "deleteEmployee"/>
            </tbody>
        </table>
    </div>
  </template>
  
  <script setup>
    import { ref } from 'vue';
    import { empList } from './employeedata';
    import EmployeeComponent from './EmployeeComponent.vue';
    

  const employees = ref(empList);
  const deleteEmployee = (empId)=> {
    for(let e of employees.value) {
        if(e.empid === empId) {
            const flag = confirm("Are you sure you want to delete this employee?");
            if(flag) {
            employees.value.splice(employees.value.indexOf(e), 1);
            }
            break;
        }
    }
  }


  </script>