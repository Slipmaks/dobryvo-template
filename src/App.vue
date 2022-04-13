<template>
  <div class="wrapper">
    <Menu />
    <Form />
  </div>
  <div class="slider"><Slider /></div>

  <Information />
</template>
<script>
import Slider from "./components/Slider.vue";
import Form from "./components/Form.vue";
import Menu from "./components/Menu.vue";
import Information from "./components/Information.vue";
export default {
  components: {
    Slider,
    Form,
    Menu,
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
  max-width: 1000px;
  margin-left: auto;
  margin-right: auto;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  z-index: 1;
}
.slider {
  position: absolute;
  top: 0px;
  z-index: 2;
}
</style>
