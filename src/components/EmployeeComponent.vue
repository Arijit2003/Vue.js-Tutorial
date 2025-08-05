<template>

<tr>
    <td>{{ emp.empid }}</td>
    <td>{{ emp.empName }}</td>
    <td>{{ emp.salary }}</td>
    <td>{{ emp.deptName }}</td>
    <td> 
        <button type="button" @click="sendEmpIdToDelete">Delete</button>
    </td>
</tr>

</template>


<script lang="ts" setup>

    import { defineProps, defineEmits } from 'vue';

    const emit = defineEmits(['deleteEmp']);

    const props = defineProps<{
        emp:{
            empid: number;
            empName: string;
            salary: number;
            deptName: string;
        }
    }>();

    const sendEmpIdToDelete = () => {
        emit('deleteEmp', props.emp.empid);
    }






</script>