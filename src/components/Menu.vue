<template>
  <div>
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
  height: 20px;
}
header select:focus-visible {
  outline: none;
}
select option {
  color: black;
  background-color: rgb(255, 162, 0);
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
  width: 100%;
  justify-content: center;
  text-align: center;
  border: 1px solid #bab2a7;
}

menu li {
  width: fit-content;
  padding-right: 22px;
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
  padding-left: 7.5px;
}

.basket {
  cursor: pointer;
  font-size: 14px;
  font-family: "Roboto Condensed";
  font-weight: bold;
  border: none;
  display: flex;
  align-items: center;
  padding: 0 59px;
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
.menu-wrapper {
  top: 58px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
@media (max-width: 1140px) {
  menu {
    display: none;
  }
}
@media (max-width: 767px) {
  header h1 {
    font-size: 30px;
  }
  header li {
    font-size: 10px;
  }
  nav ul {
    padding-right: 0;
    display: flex;
    flex-direction: column;
  }
}
</style>
