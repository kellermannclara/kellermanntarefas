<script setup>
    defineEmits(['Adicionar'])
</script>
<template>

    <button @click.prevent="$emit('Adicionar')">
        <slot></slot>
    </button>

</template>
<style scoped></style>