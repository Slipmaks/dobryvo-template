<template>
  <div class="overview">
    <div class="bottle-info">
      <img
        class="bottle"
        src="../assets/evergeen-souse/bottle.png"
        alt="bottle"
      />
      <div>
        <pre><h1>ОРГАНИЧЕСКОЕ
       НАНО-УДОБНИЕ 
           ДОБРИВО</h1></pre>

        <ul>
          <li>
            <h3>ПРИРОСТ УРАЖАЯ</h3>
            <p>в сравнении с химическим удобрением</p>
            <h4>30%-250%</h4>
          </li>
          <li>
            <h3>ЭКОНОМИЯ</h3>
            <p>химических удобрений в хозяйстве</p>
            <h4>до 70%</h4>
          </li>
          <li>
            <h3>РОСТ КОРНЕВОЙ</h3>
            <p>системы растений при использовании</p>
            <h4>в 3-10раз</h4>
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
  padding-top: 40px;
  list-style-image: url(../assets/evergeen-souse/star.png);
  display: flex;
  flex-direction: column;
  padding-left: 60px;
}
ul li::marker {
  font-size: 10px;
}

.overview h2 {
  float: left;
  font-size: 40px;
  color: #25383f;
  font-family: "Roboto Condensed";
  word-wrap: anywhere;
}
.bottle-info h1 {
  overflow-wrap: break-word;

  font-family: "Roboto Condensed";
  font-weight: bold;
  line-height: 48px;
  color: white;
  font-size: 60px;
  padding-left: 90px;
}
.bottle-info h3 {
  font-family: "Roboto Condensed";
  font-weight: bold;
  font-size: 25.16px;
}
.bottle-info h4 {
  font-family: "Roboto";
  font-weight: normal;
  font-size: 35.16px;
  color: #c49a6c;
}
.bottle-info p {
  font-family: "Roboto";
  font-weight: normal;
  font-size: 11px;
}
.detail {
  display: flex;
  align-items: flex-end;
  flex-direction: column;
}
.bottle {
  top: 30px;
  float: left;
  shape-outside: url(../assets/evergeen-souse/bottle.png);
  height: 345px;
  width: 191px;
  margin-top: 100px;
}
</style>
