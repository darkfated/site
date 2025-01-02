<script setup>
import { inject, computed } from 'vue';
import Tab from './Tab.vue'
import Info from './Tabs/Info.vue'
import Games from './Tabs/Games.vue'
import Films from './Tabs/Films.vue'
import Contacts from './Tabs/Contacts.vue'

const { currentTab, _ } = inject('currentTab');
const showInfo = computed(() => currentTab.value == 1);
const showGames = computed(() => currentTab.value == 2);
const showFilms = computed(() => currentTab.value == 3);
const showContacts = computed(() => currentTab.value == 4);
</script>

<template>
    <div class='main'>
        <Tab title='Информация 📌' v-if='showInfo'>
            <Info></Info>
        </Tab>
        <Tab title='Пройденные игры 👑' v-if='showGames'>
            <Games></Games>
        </Tab>
        <Tab title='Рецензии на фильмы 📽️' v-if='showFilms'>
            <Films></Films>
        </Tab>
        <Tab title='Связь со мной 🧾' v-if='showContacts'>
            <Contacts></Contacts>
        </Tab>
    </div>
</template>

<style scoped>
.main {
    width: calc(100% - 336px);
    height: calc(100% - 16px);
    position: absolute;
    left: 320px;
    top: 0;
    margin: 8px;
}
</style>
