<script setup>
defineProps(['title', 'description'])
defineEmits(['alertInfo'])
</script>
<template>
    <div class="kotak">
        <h3>{{ title }}</h3>
        <slot name="slot1"></slot>
        <p>{{ description }}</p>
        <slot name="slot2"></slot>
        <button @click="$emit('alertInfo', title, description)">alert</button>
        <slot name="slot3"></slot>
    </div>
</template>

<style scoped>
.kotak {
    border: solid 1px;
    width: 200px;
    padding: 0px 10px;
    margin: 10px;
    display: inline-block;
}
button {
    margin-bottom: 10px;
}
</style>