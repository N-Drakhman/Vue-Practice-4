<script setup>
import { ref, computed } from "vue";

const login = defineModel(login);
const password = defineModel(password);
const callCounter = 0;

function getValidityMessage() {
  if (password.value?.length < 8) {
    return "Passowrd must be at least 8 characters";
  }

  return "All good";
}

const ValidityMessage = computed(() => {
  callCounter++;

  if (password.value?.length < 8) {
    return "Passowrd must be at least 8 characters";
  }

  return "All good";
});

// const ValidityMessage = computed(    {
//   get(){
// if (password.value?.length < 8) {
//     return "Passowrd must be at least 8 characters";
//   }

//   return "All good";
//   }

//   set(value){
// console.log('setter called:' + value )
//   }
// });
</script>

<template>
  <input type="text" placeholder="login" v-model="login" />
  <input type="text" placeholder="password" v-model="password" />

  <span>{{ getValidityMessage() }}</span>
  <span>{{ ValidityMessage }}</span>
</template>
