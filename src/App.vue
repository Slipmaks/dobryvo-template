<template>
  <Slider />
  <Form />
</template>
<script>
import Slider from "./components/Slider.vue";
import Form from "./components/Form.vue";

export default {
  components: {
    Slider,
    Form,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}
</style>
