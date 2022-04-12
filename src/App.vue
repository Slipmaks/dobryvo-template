<template>
  <Menu />
  <Slider />
  <Form />
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
}
</style>
