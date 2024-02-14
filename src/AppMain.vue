<script>
export default {
  props: { obj: Object },
};
</script>

<template>
  <h4 v-if="obj.titolo != '22'" :class="obj.numero > 4 ? 'red' : ''">
    {{ obj.numero + 1 }} {{ obj.titolo }}
  </h4>
</template>

<style scoped>
.red {
  color: red;
}
</style>
