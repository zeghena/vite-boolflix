<script>
import axios from "axios";
import { store } from "./store";
export default {
  data() {
    return {
      // store,
      searchedTerm: "ciao",
      movies: [],
    };
  },
  methods: {
    performSearch() {
      axios
        .get("https://api.themoviedb.org/3/search/movie", {
          params: {
            // api_key: "eea25a56cc9e118410332122c6687028",
            api_key: "3eaba1ac85ce1e4f8d358abb6cdcd712",
            query: this.searchedTerm,
          },
        })
        .then((response) => {
          console.log(response.data.results);
          this.movies = response.data.results;
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
    <div v-for="movie in movies">{{ movie.original_title }}</div>
  </div>
</template>

<style lang="scss">
// todo: use scss
@use "./styles/general.scss";
</style>
