<template>
  <div>
    <div
      v-for="(option,index) in options"
      :key="index"
    >
      <label
        class="element-animation1 btn btn-lg btn-light btn-block"
        @click="select(index)"
      ><span class="btn-label"><i class="glyphicon glyphicon-chevron-right"></i></span>{{option}}</label>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    options: Array
  },
  methods: {
    select(value) {
      console.log(value)
    }
  }
};
</script>

<style>
label.btn {
  padding: 18px 60px;
  white-space: normal;
  margin-bottom: 0px;
}

label.btn:hover {
  text-shadow: 0 3px 2px rgba(0, 0, 0, 0.4);
}
label.btn-block {
  text-align: left;
  position: relative;
}

label .btn-label {
  position: absolute;
  left: 0;
  top: 0;
  display: inline-block;
  background: rgba(0, 0, 0, 0.15);
  height: 100%;
}
label .glyphicon {
  top: 34%;
}
.element-animation1 {
  animation: animationFrames ease 0.8s;
  animation-iteration-count: 1;
  transform-origin: 50% 50%;
  -webkit-animation: animationFrames ease 0.8s;
  -webkit-animation-iteration-count: 1;
  -webkit-transform-origin: 50% 50%;
  -ms-animation: animationFrames ease 0.8s;
  -ms-animation-iteration-count: 1;
  -ms-transform-origin: 50% 50%;
}
.element-animation2 {
  animation: animationFrames ease 1s;
  animation-iteration-count: 1;
  transform-origin: 50% 50%;
  -webkit-animation: animationFrames ease 1s;
  -webkit-animation-iteration-count: 1;
  -webkit-transform-origin: 50% 50%;
  -ms-animation: animationFrames ease 1s;
  -ms-animation-iteration-count: 1;
  -ms-transform-origin: 50% 50%;
}
.element-animation3 {
  animation: animationFrames ease 1.2s;
  animation-iteration-count: 1;
  transform-origin: 50% 50%;
  -webkit-animation: animationFrames ease 1.2s;
  -webkit-animation-iteration-count: 1;
  -webkit-transform-origin: 50% 50%;
  -ms-animation: animationFrames ease 1.2s;
  -ms-animation-iteration-count: 1;
  -ms-transform-origin: 50% 50%;
}
.element-animation4 {
  animation: animationFrames ease 1.4s;
  animation-iteration-count: 1;
  transform-origin: 50% 50%;
  -webkit-animation: animationFrames ease 1.4s;
  -webkit-animation-iteration-count: 1;
  -webkit-transform-origin: 50% 50%;
  -ms-animation: animationFrames ease 1.4s;
  -ms-animation-iteration-count: 1;
  -ms-transform-origin: 50% 50%;
}
</style>