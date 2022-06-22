<template>
  <div id="app">
    <!-- <list-item @increment="increment"></list-item> -->
    <list-item></list-item>
    {{ count1 }}
    <!-- <input type="text" @change="text = $event">
  <input type="text" @input="text = $event"> -->
    <!-- <input type="text" @keyup.alt.67="increment" /> {{ count2 }} -->
    <!-- <button @click="count1++">Click1 {{count1}}</button>
    <button @click="increment">Click2 {{count2}}</button>
    <button @click="increment3(2, $event)">Click3 {{count3}}</button> -->
    <!-- <button @click.ctrl="increment">CLICK</button> -->
  </div>
</template>
<script>
import ListItem from "./components/ListItem.vue";
export default {
  name: "App",
  data() {
    return {
      text: "",
      count1: 0,
      count2: 0,
      count3: 0,
    };
  },

  created(){
    this.$root.$on('increment', this.increment);
  },
  components: {
    ListItem,
  },
  method: {
    increment(valor,event) {
      this.count += valor;
      alert(event);

      console.log("123123123123");
    },
    // increment() {
    //   this.count1++;
    // },
    // increment() {
    //   this.count2++;
    // },
    // increment2(val, event) {
    //   alert(event);
    //   this.count3 += val;
    // },
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
