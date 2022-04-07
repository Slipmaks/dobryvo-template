<template>
  <div class="menu">
    <header>
      <div><h1>ДОБРИВО</h1></div>
      <nav>
        <ul>
          <li>ОПЛАТА И ДОСТАВКА</li>
          <li>НОВОСТИ</li>
          <li>СПРАВОЧНИК</li>
          <li>СЕРТИФИКАТЫ</li>
        </ul>
        <select>
          <option>RU</option>
          <option>UA</option>
        </select>
      </nav>
    </header>
    <menu>
      <ul>
        <li>НАГРО-УДОБРЕНИЕ</li>
        <li>БИОДИЗЕЛЬ</li>
        <li>СИЛЬКО</li>
        <li>ИИНТЕРНЕТ-МАГАЗИН</li>
        <li>ВОПРОСЫ-ОТВЕТЫ</li>
        <li>КОНТАКТЫ</li>
        <li class="basket">КОРЗИНА</li>
      </ul>
    </menu>
  </div>
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

export default {
  components: {
    Splide,
    SplideSlide,
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
header {
  display: flex;
  align-items: center;
  justify-content: space-around;
}
header li,
menu li {
  list-style: none;
  display: inline-block;
}
nav {
  display: flex;
}
nav li {
  padding: 10px;
}
menu {
  display: flex;
  justify-content: center;
}
menu ul {
  border: 1px solid grey;
}
menu li {
  padding: 10px;
  background: linear-gradient(
    0deg,
    rgba(242, 243, 243, 1) 0%,
    rgba(253, 253, 253, 1) 100%
  );
}
.menu {
  width: 100%;
  position: absolute;
  z-index: 1;
}
.basket {
  background: linear-gradient(
    0deg,
    rgba(117, 91, 30, 1) 0%,
    rgba(84, 164, 40, 1) 100%
  );
}
</style>
