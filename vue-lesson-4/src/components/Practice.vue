<script setup>
import { reactive, computed } from "vue";

const props = defineProps({
  user: { type: Object, required: true },
  text: { type: String, default: "details" },
});

const userInfo = computed(() => {
  return `name: ${props.user.name}, age: ${props.user.age}, location: ${props.user.location}`;
});
</script>

<template>
    <div class="user-info">
      <slot name="default" :userInfo="userInfo"></slot>
    </div>

    <slot name="button">
      <button>show details</button>
    </slot>
</template>

<style>
.user-info {
  display: block;
  padding: 7px 12px;
  border-radius: 8px;

  color: white;
  background-color: #323232;
}

button {
  color: #fff;
  background: linear-gradient(315deg, #42d392 25%, #647eff);
  border: none;
  margin: 5px;
  border-radius: 8px;
  cursor: pointer;
  padding: 7px 12px;
}
</style>
