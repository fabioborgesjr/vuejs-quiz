<template>
  <div
    class="alert alert-primary"
    role="alert"
    v-show="right"
    :data-resultado="right"
  >
    Você acertou {{right}} questões
  </div>
</template>

<script>
export default {
  props: {
    right: Number
  }
};
</script>

<style>
</style>