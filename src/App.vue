<template>
  <div class="global-wrapper">
    <div class="wrapper">
      <div class="cont-1"><Menu /></div>
      <div class="cont-2">
        <Overview />
      </div>
      <div class="cont-3"><Form /></div>
    </div>
    <Slider />
    <BackgroundBody />
  </div>
</template>
<script>
import Slider from "./components/Slider.vue";
import Menu from "./components/Menu.vue";
import BackgroundBody from "./components/BackgroundBody.vue";
import Form from "./components/Form.vue";
import Overview from "./components/Overview.vue";
export default {
  components: {
    Slider,
    Menu,
    BackgroundBody,
    Form,
    Overview,
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
  position: absolute;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  max-width: 1000px;
  left: 0;
  right: 0;
  margin-left: auto;
  margin-right: auto;
  z-index: 2;
}
.cont-1 {
  padding-top: 57px;
  padding-bottom: 68px;
  grid-column-start: 1;
  grid-column-end: 3;
}
.cont-3 {
  justify-self: end;
}
.cont-2 h1 {
  font-family: "Roboto Condensed";
  font-weight: bold;
  line-height: 48px;
  color: white;
  font-size: 60px;
}
.global-wrapper {
  width: 90%;
  max-width: 1200px;
  margin-left: auto;
  margin-right: auto;
}
@media (max-width: 1140px) {
  .global-wrapper {
    width: 100%;
  }
  .wrapper {
    width: 90%;
  }
}
</style>
