<template>
  <div class="box">
    <textarea name="respostaEdicao"  :placeholder="placeholder" v-model="textoAlterado"></textarea>
  </div>
</template>

<script lang="ts">
  import { defineComponent } from "vue";

  export default defineComponent({
    name: "EdicaoRespostaComponent",
    props: {
        textoAtual: {
            type: String,
            required: true
        }
    },
    data(){
      return{
        placeholder: 'Ao clicar em Copiar sua resposta será colada aqui.'
      }
    },
    computed:{
        textoAlterado(){
            return this.textoAtual
        }
    }
  });
</script>

<style scoped>
textarea{
    border-radius: 5px;
    padding: 1rem;
    border: none;
    width: 50vw;
    height: 50vh;
}
</style>