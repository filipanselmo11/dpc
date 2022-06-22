<template>
  <div id="app">
    <ul>
      <list-item v-for="(index, todo) in todos" :key="index" v-bind="todo">
        <!-- {{todo}} -->
      </list-item>
      <!-- <list-item 
        v-for="(index, todo) in todos" 
        :key="index"
        :todo="todo">
      </list-item> -->

      <!-- <template v-if="!todo.isCompleted">
        <li v-for="(index, todo) in todos" :key="index">
          {{ todo }}
        </li>
      </template>
      <li v-else>
        Items
      </li> -->
      <!-- <template v-if="todos.lenght > 0">
        <li v-for="(index, todo) in todos" :key="index">
          {{ todo }}
        </li>
      </template>
      <li v-else>No item</li> -->
      <!-- <li v-for="(valor, chave, index) in todos" :key="chave">
        {{ chave }} : {{ valor }} - {{ index }}
      </li> -->
      <!-- <li v-for="(item, index) in todos" :key="index">
        {{ item }} {{index }}
      </li> -->
    </ul>
  </div>
</template>

<script>
import ListItem from "./components/ListItem.vue";
export default {
  name: "App",
  data() {
    return {
      // todos: ["1", "2", "3"],
      // todos:{
      //   item1: '1',
      //   item2: '2',
      //   item3: '3',
      // }
      // todos: [
      //   { label: "Todo 1", isCompleted: true },
      //   { label: "Todo 2", isCompleted: true },
      //   { label: "Todo 3", isCompleted: false },
      //   { label: "Todo 4", isCompleted: false },
      // ],
      todos: [
        { label: "Item-1", value: 1 },
        { label: "Item-2", value: 2 },
        { label: "Item-3", value: 3 },
        { label: "Item-4", value: 4 },
        { label: "Item-5", value: 5 },
      ],
    };
  },
  components: { ListItem },
  computed: {
    filteredTodos() {
      return this.todos.filter((todo) => !todo.isCompleted);
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
