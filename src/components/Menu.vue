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
      <button class="basket">КОРЗИНА</button>
    </menu>
  </div>
</template>

<style>
header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  color: white;
  font-weight: 100;
  padding-bottom: 10px;
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
nav ul {
  padding-right: 90px;
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
  border: 1px solid #bab2a7;
}

menu li {
  padding-right: 24.9px;
  color: #6d6e71;
  height: 45px;

  font-family: "Roboto Condensed";
  font-weight: bold;
  background: linear-gradient(
    0deg,
    rgb(241, 242, 242) 0%,
    rgba(253, 253, 253, 1) 100%
  );
  align-items: center;
  justify-content: center;
}
menu li::after {
  content: "▶";
  font-size: 7px;
  padding-left: 8px;
}

.basket {
  cursor: pointer;
  font-size: 14px;
  font-family: "Roboto Condensed";
  font-weight: bold;
  border: none;
  display: flex;
  align-items: center;
  padding: 0 49px;
  color: white;
  background: linear-gradient(
    0deg,
    rgba(117, 91, 30, 1) 0%,
    rgba(84, 164, 40, 1) 100%
  );
}
.basket::before {
  content: url(../assets/evergeen-souse/basket.png);
  padding-right: 8px;
}
.basket::after {
  content: "";
}
menu li:first-child {
  padding-left: 40px;
}
.wrapper {
  top: 58px;
  position: absolute;
  max-width: 1000px;
  left: 0;
  right: 0;
  margin-left: auto;
  margin-right: auto;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  z-index: 1;
}
</style>
