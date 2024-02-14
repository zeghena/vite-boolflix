<script>
import AppMain from "./AppMain.vue";
export default {
  data() {
    return {
      msg: "Messaggio urgente",
      array: [
        { numero: 2, titolo: "sadsad" },
        { numero: 1, titolo: "22" },
        { numero: 5, titolo: "asddsa" },
      ],
    };
  },
  components: { AppMain },
};
</script>

<template>
  <h1>{{ msg }}</h1>
  <AppMain v-for="testo in array" :obj="testo" />
</template>

<style lang="scss">
@use "./styles/general.scss";
</style>
