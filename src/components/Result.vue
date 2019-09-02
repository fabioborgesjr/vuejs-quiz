<template>
  <div v-show="started">
    <div
      class="alert alert-primary"
      role="alert"
      :data-resultado="right"
    >
      Você acertou <b>{{right}}</b> questões
    </div>
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    right: Number,
    started: Boolean
  }
};
</script>

<style>
</style>