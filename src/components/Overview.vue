<template>
  <div class="overview">
    <h1>ОРГАНИЧЕСКОЕ НАНО-УДОБНИЕ ДОБРИВО</h1>
    <div class="bottle-info">
      <img src="../assets/evergeen-souse/bottle.png" alt="" />
      <div>
        <ul>
          <li>
            <h3>ПРИРОСТ УРАЖАЯ</h3>
            <p>в сравнении с химическим удобрением</p>
            <h3>30%-250%</h3>
          </li>
          <li>
            <h3>ЭКОНОМИЯ</h3>
            <p>химических удобрений в хозяйстве</p>
            <h3>до 70%</h3>
          </li>
          <li>
            <h3>РОСТ КОРНЕВОЙ</h3>
            <p>системы растений при использовании</p>
            <h3>в 3-10раз</h3>
          </li>
        </ul>
      </div>
    </div>
    <div class="detail">
      <pre><h2>УЗНАЙТЕ 
О НАГРО БОЛЬШЕ!</h2></pre>
      <button>УЗНАТЬ БОЛЬШЕ</button>
    </div>
  </div>
</template>
<style scoped>
ul {
  list-style-image: url(../assets/evergeen-souse/star.png);
}
ul li::marker {
  font-size: 10px;
}
.bottle-info {
  display: flex;
  justify-content: space-between;
}
.overview h2 {
  font-size: 40px;
  color: #25383f;
  font-family: "Roboto Condensed";
}
.detail {
  float: right;
  display: flex;

  align-items: flex-end;
  flex-direction: column;
}
</style>
