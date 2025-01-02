<script setup>
defineProps({
    title: String
});
</script>

<template>
    <div class='header'>
        <p>{{ title }}</p>
    </div>
    <slot></slot>
</template>

<style scoped>
.header {
    height: 60px;
    background-color: var(--color-theme);
    border-radius: 8px;
    display: flex;
    align-items: center;
}

.header p {
    margin-left: 18px;
    font-size: 20px;
}
</style>
