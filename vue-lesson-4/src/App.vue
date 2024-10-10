<script setup>
import Practice from "./components/Practice.vue";
</script>

<template>
  <Practice
    :user="{ name: 'George', age: 28, location: 'US, Texas, Lakeside' }"
  >
    <template #default="{ userInfo }">
      <p>{{ userInfo }}</p>
    </template>

    <template #button>
      <button>details</button>
    </template>
  </Practice>
</template>

<style scoped></style>
