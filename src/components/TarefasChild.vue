<script setup>
defineProps(['desc', 'id', 'status'])
defineEmits(['editar', 'excluir'])
</script>

<template>

    <li v-for="item in tarefasFiltradas" :key="item.id" @click="marcarConcluida(item.id)"
        :class="{ concluida: item.status === 'concluida' }">
        {{ item.desc }}

        <span>
          <button @click.prevent.stop="deletar(item.id)">Deletar</button>
          <button @click.stop="editarTarefa(item)">Editar</button>
        </span>

    </li>

</template>

<style scoped></style>