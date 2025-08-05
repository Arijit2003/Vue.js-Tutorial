<template>
    <h1>Child Component</h1>
    <h2>Message from Parent: {{ cmessage }}</h2>
    <button @click="sendMessageToParent"> Message Parent </button>
</template>

<script setup lang="ts">
import { defineProps, defineEmits } from 'vue';

// Define props for the child component
const props = defineProps<{
    cmessage: string; // cmessage is a string prop passed from the parent
}>();

const emit = defineEmits(['reply']) // reply is an event name that can be emitted to the parent

const sendMessageToParent = () => {
    // Emit an event to the parent with a message
    emit('reply', 'Hello Parent, I am your Child');
}

</script>