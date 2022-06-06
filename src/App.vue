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
  box-sizing: border-box;
}
body {
  font-family: "Roboto";
  font-size: 14px;
  background: #f1f2f2;
}
.wrapper {
  position: absolute;
  display: grid;
  grid-template-columns: 60% 40%;
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
@media (max-width: 926px) {
  .wrapper {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .cont-1 {
    padding-top: 20px;
    padding-bottom: 30px;
    grid-column-start: 1;
    grid-column-end: 3;
  }
  .cont-2 h1 {
    font-size: 36px;
    line-height: 28px;
  }
  .cont-3 {
    display: flex;
    justify-content: center;
  }
}
</style>
