<script setup>
const links = [
  { name: 'GitHub', url: 'https://github.com/darkfated' },
  { name: 'YouTube канал', url: 'https://youtube.com/@darkfated' },
  { name: 'Steam профиль', url: 'https://steamcommunity.com/id/darkfated/' },
  { name: 'Группа Telegram', url: 'https://t.me/darkfated_group' },
  { name: 'Поддержка донатом', url: 'https://www.donationalerts.com/r/darkfated' },
]
</script>

<template>
  <div class='cards'>
    <div class='card' v-for='link in links'>
      <div class='card__header'>
        <p><a :href="link.url" target='_blank'>{{ link.name }}</a></p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.cards {
  margin: 8px;
  display: grid;
  gap: 8px;
  grid-template-columns: repeat(4, 1fr);
}

.card {
  height: 300px;
  background-color: #2d2d2d;
  border: 0;
  border-radius: 16px;
  transition: 0.25s;
}

.card:hover {
  margin: 6px;
}

.card__header {
  width: 100%;
  height: 40px;
  background-color: #3f3f3f;
  border-radius: 8px 8px 0 0;
  text-align: center;
}

.card__header p {
  transform: translate(0, 50%);
  font-size: 18px;
  user-select: none;
}

.card__header p a,
a:active {
  color: white;
  text-decoration: none;
  transition: 0.25s;
}

.card__header p a:hover {
  color: black;
}
</style>
