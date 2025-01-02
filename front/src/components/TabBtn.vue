<script setup>
import { inject } from 'vue';

const { currentTab, updateCurrentTab } = inject('currentTab')
const props = defineProps({
  tabId: Number
})

</script>

<template>
  <button @click='updateCurrentTab(tabId)'>
    <slot></slot>
  </button>
</template>

<style scoped>
button {
  display: block;
  width: calc(100% - 16px);
  margin: 8px;
  height: 36px;
  background-color: transparent;
  color: white;
  font-size: 18px;
  border: 0;
  border-radius: 6px;
  cursor: pointer;
}

button:hover {
  background-color: var(--color-theme);
  transition: 0.1s;
}

button:not(:hover) {
  transition: 0.3s;
}
</style>
