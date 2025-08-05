<template>
    <h1>Parent Component</h1>
    <h2>Message from Child :- {{ childMessage }}</h2>
    <ChildComponent :cmessage="parentMessage" @reply = "receiveMessageFromChild"/>
</template>

<script setup>
import { ref } from 'vue';
import ChildComponent from './ChildComponent.vue';

// Define the reactive parent message
const parentMessage = ref('Hello My Child');
const childMessage = ref('')

const receiveMessageFromChild = (message)=>{
    childMessage.value = message;
}
</script>