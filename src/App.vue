<template>
  <Menu />
  <Slider />
  <Form />
</template>
<script>
import Slider from "./components/Slider.vue";
import Form from "./components/Form.vue";
import Menu from "./components/Menu.vue";
export default {
  components: {
    Slider,
    Form,
    Menu,
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
}
</style>
