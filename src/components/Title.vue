<template>
  <div>
    <h1 v-bind="$attrs">{{ titulo }}</h1>
    <h2>{{ subtitulo }}</h2>
    <h3>{{ tipo }}</h3>
    <!-- <Subtitle v-bind="$props" -->
  </div>
</template>

<script>
export default {
  name: "Title",
  inheritAttrs: false,
  prpos: {
    titulo: {
      type: String,
      required: true,
    },
    subtitulo: {
      type: String,
      required: false,
      default: "Olá Mundo",
    },
    tipo: {
      type: Number,
      validador(value) {
        return [1, 2, 3].includes(value);
      },
    },
  },
};
</script>

<style></style>
