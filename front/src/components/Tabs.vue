<script setup>
import TabBtn from './TabBtn.vue'
</script>

<template>
  <div class='tabs'>
    <TabBtn :tabId="1">Информация</TabBtn>
    <TabBtn :tabId="2">Пройденные игры</TabBtn>
    <TabBtn :tabId="3">Рецензии на фильмы</TabBtn>
    <TabBtn :tabId="4">Контакты</TabBtn>
    <span class='info'>DarkFated 2024</span>
  </div>
</template>

<style scoped>
.tabs {
  position: absolute;
  top: 0;
  left: 0;
  width: 320px;
  height: 100%;
  background-color: #101011;
}

.info {
  color: #cccccc;
  position: absolute;
  bottom: 8px;
  left: 50%;
  transform: translate(-50%, 0)
}
</style>
