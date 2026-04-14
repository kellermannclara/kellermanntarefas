<script setup>
const props = defineProps(['desc', 'id', 'status'])
const emit = defineEmits(['toggle', 'delete', 'edit'])
</script>

<template>

    <li @click="emit('toggle', id)" :class="{ concluida: status === 'concluida' }">
        {{ desc }}

        <span>
            <button @click.stop="emit('delete', id)">Deletar</button>
            <button @click.stop="emit('edit', id)">Editar</button>
        </span>
    </li>

</template>

<style scoped>

li {
    display: flex;
    justify-content: space-between;
}


</style>