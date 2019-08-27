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
      <p class="card-text">{{question}}</p>
    </div>
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