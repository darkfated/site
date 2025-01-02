<script setup>
import { inject, computed } from 'vue';
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
        <Info v-if='showInfo'></Info>
        <Games v-if='showGames'></Games>
        <Films v-if='showFilms'></Films>
        <Contacts v-if='showContacts'></Contacts>
    </div>
</template>

<style scoped>
.main {
    width: calc(100% - 336px);
    height: calc(100% - 16px);
    position: absolute;
    left: 320px;
    margin: 8px;
}
</style>
