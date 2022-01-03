<template>
  <div class="input-group">
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

</style>