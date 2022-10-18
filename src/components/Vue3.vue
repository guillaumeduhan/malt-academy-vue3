<script setup>
import { ref, onMounted, watch } from "vue";
// import { useMouse } from "../composables/useMouse";

// const { x, y } = useMouse();

let message = ref("No message yet");

const sayHello = () => {
  message.value = "Hello world !";
};

onMounted(() => {
  console.log("mounted");
});

watch(message, () => console.log("message has changed"));
</script>

<template>
  <div>
    <p>{{ message }}</p>
    <button @click="sayHello">Change message</button>
  </div>
</template>
