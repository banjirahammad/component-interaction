<script setup>
import { ref } from 'vue';
import ParentComponent from "./components/ParentComponent.vue";
const message = ref("Hello I'm from Parent Component!");

</script>

<template>
  <div
    class="bg-gradient-to-r from-pink-100 via-indigo-100 to-pink-100 h-screen flex flex-col justify-center items-center text-center">
    <ParentComponent :message="message" />
  </div>
</template>

<style scoped></style>