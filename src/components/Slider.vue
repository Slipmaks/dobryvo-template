<template>
  <Menu />
  <Splide :options="options">
    <SplideSlide>
      <img src="../assets/evergeen-souse/Header.png" alt="" />
    </SplideSlide>
    <SplideSlide>
      <img src="../assets/evergeen-souse/Header.png" alt="" />
    </SplideSlide>
    <SplideSlide>
      <img src="../assets/evergeen-souse/Header.png" alt="" />
    </SplideSlide>
  </Splide>
</template>
<script>
import "@splidejs/splide/dist/css/splide.min.css";
import { Splide, SplideSlide } from "@splidejs/vue-splide";
import Menu from "./Menu.vue";

export default {
  components: {
    Splide,
    SplideSlide,
    Menu,
  },
  setup() {
    const options = {
      rewind: true,
      gap: "1rem",
      autoplay: true,
      speed: 3000,
      arrows: false,
      pagination: true,
    };

    return { options };
  },
};
</script>
<style>
.splide__slide img {
  width: 100%;
}
</style>
