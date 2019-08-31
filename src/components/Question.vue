<template>
  <div
    class="card"
    style="width: 100%;"
  >
    <img
      :src="alt"
      class="card-img-top"
      :alt="alt"
    >
    <div class="card-body">
      <p class="card-text lead">{{question}}</p>
    </div>
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    question: "",
    imgSrc: "",
    alt: ""
  }
};
</script>

<style>
</style>