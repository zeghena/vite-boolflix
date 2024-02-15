<script>
import axios from "axios";
import { store } from "./store";
export default {
  data() {
    return {
      // store,
      searchedTerm: "ciao",
    };
  },
  methods: {
    performSearch() {
      axios.get("...").then((response) => {
        console.log(response.data);
      });
    },
  },
};
</script>

<template>
  <div class="container mt-5">
    <div class="d-flex">
      <input
        type="text"
        class="form-control"
        v-model="searchedTerm"
        @keyup.enter="performSearch()"
      />
      <button class="btn btn-primary" @click="performSearch()">Ricerca</button>
    </div>
  </div>
</template>

<style lang="scss">
// todo: use scss
@use "./styles/general.scss";
</style>
