<script>
import { store } from "./store";
export default {
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <div class="container mt-5">
    <input type="text" class="form-control" />
    <button class="btn btn-primary"></button>
  </div>
</template>

<style lang="scss">
// todo: use scss
@use "./styles/general.scss";
</style>
