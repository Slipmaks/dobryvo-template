<template>
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
</style>
