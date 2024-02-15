<script>
import { store } from "./store";
export default {
  data() {
    return {
      store,
      title: "Messaggio urgente",
    };
  },
};
</script>

<template>
  <h1>{{ title }}</h1>
</template>

<style lang="scss">
// todo: use scss
@use "./styles/general.scss";
</style>
