<template>
  <div id="app">
    <!-- <Title titulo="Título 1"/>
    <Title titulo="Título 2"/> 
    Não precisar usar bind para strings-->
    <!-- <Title :titulo="1"></Title>
    <Title :titulo="122"></Title> -->
    <Title v-bind="titulos[0]"></Title>
    <!-- <Title class="red" style="display: block;" titulo="Vue js" :tipo="1"></Title> -->
    <!---Precisa usar o bind para outros tipos de dados, como numeros por exemplo-->
  </div>
</template>

<script>
import Title from "./components/Title.vue";
export default {
  components: { Title },
  name: "App",
  data(){
    return {
      titulos:[
        { titulo: 'Titulo 1', subtitulo: 'SUBT 1', tipo: 1}
      ],
    }
  }
};
</script>

<style></style>
