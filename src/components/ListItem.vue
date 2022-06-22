<template>
  <li>{{ label }} {{ value }}</li>
</template>

<script>
export default {
  name: "ListItem",
  props: {
    // todo: Object
    label: String,
    value: [String, Number],
  },
};
</script>

<style></style>
