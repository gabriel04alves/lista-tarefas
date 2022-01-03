<template>
  <ul>
    <li
      v-for="(tarefa, index) in tarefas"
      :key="index"
      :class="{ removed: tarefa.checked }"
    >
      <input type="checkbox" v-model="tarefa.checked" />
      <label>{{ tarefa.titulo }}</label>
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    tarefas: {
      type: Array,
      default() {
        return [{ titulo: "Atividade padrão", checked: false }];
      },
    },
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Oswald&family=PT+Serif&family=Poppins:wght@100;200&family=Raleway:ital,wght@0,200;0,300;1,200&family=Roboto+Condensed:ital,wght@0,300;1,300&display=swap');  
ul li {
font-family: 'PT Serif', serif;}
</style>