<script setup>
const prop = defineProps({ data: Array });
</script>

<template>
  <tr>
    <th v-for="(cell, key) in data[0]">{{ key }}</th>
  </tr>
  <tr v-for="item in data">
    <th v-for="(cell, item) in item">
      <slot :name="key" :row="item" v-if="$slots[key]"></slot>
      <span v-else>
        {{ cell }}
      </span>
    </th>
  </tr>
</template>
