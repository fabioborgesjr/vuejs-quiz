<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <h1 class="display-4">
      {{text}}
    </h1>
  </nav>
</template>

<script>
export default {
  props: {
    text: String
  }
};
</script>

<style>
</style>