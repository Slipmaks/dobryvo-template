<template>
  <div class="wrapper">
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
      <li>НАГРО-УДОБРЕНИЕ</li>
      <li>БИОДИЗЕЛЬ</li>
      <li>СИЛЬКО</li>
      <li>ИНТЕРНЕТ-МАГАЗИН</li>
      <li>ВОПРОСЫ-ОТВЕТЫ</li>
      <li>КОНТАКТЫ</li>
      <li class="basket">КОРЗИНА</li>
    </menu>
  </div>
</template>

<style>
header,
menu {
  width: 1000px;
}
header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  color: white;
  font-weight: 100;
}
header h1 {
  font-size: 50px;
}
header li {
  font-size: 11px;
  display: inline-block;
}
header select {
  color: whitesmoke;
  padding: 0;
  margin: 0;
  background-color: transparent;
  border: 2px solid whitesmoke;
}
header li,
menu li {
  list-style: none;
  cursor: pointer;
}
nav,
menu li {
  display: flex;
}
nav li {
  padding: 0 25px 0 25px;
}
menu {
  display: flex;
  justify-content: center;
  text-align: center;
}

menu ul {
  border: 1px solid grey;
}
menu li {
  width: 100%;
  font-family: "Roboto Condensed";
  font-weight: bold;
  padding: 10px;
  background: linear-gradient(
    0deg,
    rgb(230, 230, 230) 0%,
    rgba(253, 253, 253, 1) 100%
  );
  align-items: center;
  justify-content: center;
}
.wrapper {
  top: 60px;
  width: 100%;
  position: absolute;
  z-index: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.basket {
  background: linear-gradient(
    0deg,
    rgba(117, 91, 30, 1) 0%,
    rgba(84, 164, 40, 1) 100%
  );
}
.basket::before {
  content: url(../assets/evergeen-souse/basket.png);
}
</style>
