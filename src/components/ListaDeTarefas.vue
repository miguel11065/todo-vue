<script setup>
    const props = defineProps(['tarefas'])
</script>

<template>
<ul class="mt-4 list-group">
        <li class="list-group-item" v-for="tarefa in props.tarefas">
        <input @change="evento => tarefa.finalizada = evento.target.checked" :checked="tarefa.finalizada" :id="tarefa.titulo" type="checkbox">
        <label :class="{done: tarefa.finalizada}" :for="tarefa.titulo" class="ms-3">{{tarefa.titulo}}</label>
        </li>
    </ul>
</template>

<style scoped>
    .done{
    text-decoration: line-through;
    }
</style>