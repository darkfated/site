<script setup>
import { provide, ref } from 'vue';
import Tabs from './components/Tabs.vue'
import ActiveTab from './components/ActiveTab.vue'

let currentTab = ref(1)

function updateCurrentTab(tabId) {
  currentTab.value = tabId
}

provide('currentTab', {
  currentTab,
  updateCurrentTab
})
</script>

<template>
  <Tabs></Tabs>
  <ActiveTab></ActiveTab>
</template>
