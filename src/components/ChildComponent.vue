<script setup>

defineProps(["message", "messageFromChild"]);
defineEmits(['update:messageFromChild']);


</script>

<template>
    <div class="border-double border-4 border-indigo-300 rounded p-10 shadow-2xl shadow-blue-500/20">
        <h3 class="text-2xl pb-3 font-semibold">Child Component</h3>
        <p class="mt-2 font-bold">Received Message : {{ message }}</p>
        <button @click="$emit('update:messageFromChild', 'This is a Custom message from Child!')"
            class="my-4 px-5 py-3 font-bold bg-gradient-to-r from-indigo-500 to-pink-500 hover:from-pink-600 hover:to-indigo-600 text-white rounded">
            Emit Message
        </button>
    </div>
</template>

<style scoped></style>