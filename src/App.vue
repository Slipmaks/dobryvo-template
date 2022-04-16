<template>
  <div class="wrapper">
    <div class="cont-1"></div>
    <div class="cont-2"></div>
    <div class="cont-3"></div>
  </div>
  <Slider />
  <Information />
</template>
<script>
import Slider from "./components/Slider.vue";

import Information from "./components/Information.vue";
export default {
  components: {
    Slider,

    Information,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
body {
  font-family: "Roboto";
  font-size: 14px;
  background: #f1f2f2;
}
.wrapper {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  width: 1000px;
}
</style>
