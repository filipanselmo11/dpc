<template>
  <li @click="emit">Click me</li>
</template>

<script>
export default {
  name: "ListItem",
  methods: {
    emit(event) {
      console.log(this.$root);
      //   this.$emit("increment", 4, event);
      this.$root.$emit("increment", 4, event); //evento global;
    },
  },
};
</script>

<style></style>
