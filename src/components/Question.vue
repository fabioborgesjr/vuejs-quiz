<template>
  <div class="card" style="width: 100%;">
    <img :src="question.src" class="card-img-top" :alt="question.alt" />
    <div class="card-body">
      <p class="card-text lead">Qual personagem é esse?</p>
    </div>
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    question: {
      imgSrc: String,
      alt: String
    }
  }
};
</script>

<style>
</style>