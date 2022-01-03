<template>
  <div id="ft" class="input-group">
    <entrada-dados @salvar="adicionarTarefa" v-model="novaTarefa" />
    <span class="input-group-btn">
      <button @click="adicionarTarefa" class="btn btn-primary">
        Adicionar tarefa
      </button>
    </span>
  </div>
</template>

<script>
import EntradaDados from "./templates/EntradaDados.vue";
export default {
  components: { EntradaDados },
  data() {
    return {
      novaTarefa: "",
    };
  },
  methods: {
    adicionarTarefa() {
      this.$emit("adicionarTarefa", this.novaTarefa);
      this.novaTarefa = "";
    },
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Oswald&family=PT+Serif&family=Poppins:wght@100;200&family=Raleway:ital,wght@0,200;0,300;1,200&family=Roboto+Condensed:ital,wght@0,300;1,300&display=swap');  
 #ft {
font-family: 'PT Serif', serif;}
</style>