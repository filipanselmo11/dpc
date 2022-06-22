<template>
  <div id="app">
    <h1 style="font-size: 30px" :style="[color, fontSize]">diretiva v-bind</h1>
    <!-- <h1 class="test" :class="[red, { blue: showBlue }]">Diretiva v-bind</h1> -->
    <!-- <a :href="url">SITE</a> -->
    <!-- <h1 v-if="state === 'loading'">LOADING</h1>
    <h1 v-else-if="state === 'error'">ERROR</h1>
    <h1 v-else-if="messages.length === 0">SEM DADOS</h1>
    <h1 v-else>{{ messages }}</h1> -->
    <!-- <h1 v-if="show">Diretiva V-IF</h1>
    <h1 v-else-if="!show">DIRETIVA V_ELSE_IF</h1>
    <h1 v-else>DIRETIVA V_ELSE</h1> -->
    <!-- <h1 v-show="true">Diretiva V-SHOW</h1> -->
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      showBlue: "true",
      showRed: true,
      show: false,
      state: "loading",
      messages: [],
      url: "www.google.com",
      dyamicClass: "red",
      red: "red",
      blue: "blue",
      green: "green",
      style:{ color: 'red', fontSize: '30px'},
      color: {color: 'red'},
      fontSize: { fontSize: '30px'},
    };
  },
};
</script>

<style></style>
