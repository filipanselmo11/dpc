<template>
  <div id="app">
    <Input v-model="text" />
    {{ text }}
    <!-- <input type="text" v-model.trim="text" /> -->
    <!-- <input type="text" v-model.number="text"> -->
    {{ text }}
  </div>
</template>

<script>
import Input from "./components/Input.vue";
export default {
  name: "App",
  data() {
    return {
      text: "",
    };
  },
  components: { Input },
  watch: {
    text(value) {
      console.log(value);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
