<template>
  <div class="auth-wrapper">
    <input
      type="text"
      placeholder="contraseña..."
      v-model="password"
      @input="checkInput"
      class="password-input"
    />
    <img src="/ozzy.jpeg" alt="ozzy" class="ozzy" />
  </div>
</template>

<script setup>
import { ref } from "vue";
const password = ref("");
const emit = defineEmits({
  // No validation
  click: null,

  // Validate submit event
  validInput: (input) => {
    if (input === "I Did it") {
      return true;
    } else {
      return false;
    }
  },
});

function checkInput() {
  emit("validInput", { password: password.value });
}
</script>

<style scoped>
.ozzy {
  width: 100%;
}
.auth-wrapper {
  max-width: 600px;
  max-height: 600px;
  position: relative;
}
.password-input {
  position: absolute;
  bottom: 19%;
  left: 15%;
  z-index: 2;
  height: 70px;
  background-color: white;
  color: black;
  border: none;
  border-radius: 50%;
  text-align: center;
}
</style>
