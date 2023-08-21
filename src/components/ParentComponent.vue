<script setup>
import { ref } from "vue";
import ChildComponent from "./ChildComponent.vue";
defineProps(["message"]);
const messageFromChild = ref("");

</script>

<template>
  <div class="border-double border-4 border-indigo-300 rounded p-10 shadow-2xl shadow-blue-500/20">
    <h2 class="text-4xl mb-5 font-semibold">Parrent Component</h2>
    <h1 class="font-bold text-lg mb-5">{{ messageFromChild }}</h1>
    <ChildComponent :message="message" v-model:messageFromChild="messageFromChild" />
  </div>
</template>

<style scoped></style>