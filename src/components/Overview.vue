<template>
  <div class="overview">
    <div class="bottle-info">
      <pre><h1>ОРГАНИЧЕСКОЕ
       НАНО-УДОБНИЕ 
           ДОБРИВО</h1></pre>
      <div class="bottle-detail">
        <img
          class="bottle"
          src="../assets/evergeen-souse/bottle.png"
          alt="bottle"
        />
        <div>
          <ul>
            <li>
              <span>
                <h3>ПРИРОСТ УРАЖАЯ</h3>
                <p>в сравнении с химическим удобрением</p>
                <h4>30%-250%</h4>
              </span>
            </li>
            <li>
              <span>
                <h3>ЭКОНОМИЯ</h3>
                <p>химических удобрений в хозяйстве</p>
                <h4>до 70%</h4>
              </span>
            </li>
            <li>
              <span>
                <h3>РОСТ КОРНЕВОЙ</h3>
                <p>системы растений при использовании</p>
                <h4>в 3-10раз</h4>
              </span>
            </li>
          </ul>
          <div class="detail">
            <pre><h2>УЗНАЙТЕ 
О НАГРО БОЛЬШЕ!</h2></pre>
            <a href="#">УЗНАТЬ БОЛЬШЕ</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.bottle-info {
  position: relative;
}
ul {
  padding-top: 40px;
  list-style: none;
  display: flex;
  flex-direction: column;
  padding-left: 60px;
}
li {
  display: flex;
}
ul li:before {
  --li-icon-size: 20px;
  content: "";
  display: inline-block;
  height: var(--li-icon-size);
  width: var(--li-icon-size);
  background-size: var(--li-icon-size);
  background-image: url(../assets/evergeen-souse/star.png);
  background-repeat: no-repeat;
  margin-right: 5px;
}

.overview h2 {
  position: relative;
  float: left;
  font-size: clamp(1.125rem, 0.4rem + 3.5vw, 2.625rem);
  color: #25383f;
  font-family: "Roboto Condensed";
  word-wrap: anywhere;
}
.bottle-info h1 {
  margin: 0 auto;
  width: fit-content;
  overflow-wrap: break-word;
  font-family: "Roboto Condensed";
  font-weight: bold;
  line-height: clamp(0.875rem, 0.4rem + 3.5vw, 3rem);
  color: white;
  font-size: clamp(1.125rem, 0.7rem + 3.5vw, 3.75rem);
  padding-left: 90px;
}
.bottle-info h3 {
  display: block;
  font-family: "Roboto Condensed";
  font-weight: bold;
  font-size: clamp(0.9rem, 0.7rem + 3.5vw, 1.5725rem);
}
.bottle-info h4 {
  font-family: "Roboto";
  font-weight: normal;
  font-size: clamp(0.9rem, 0.7rem + 3.5vw, 2.1975rem);
  color: #c49a6c;
}
.bottle-info p {
  font-family: "Roboto";
  font-weight: normal;
  font-size: 11px;
}
.detail {
  display: flex;
  padding-left: 60px;
  padding-top: 40px;
  flex-direction: column;
}
.bottle {
  display: block;
  top: 30px;
  float: left;
  shape-outside: url(../assets/evergeen-souse/bottle.png);

  max-width: 191px;
  /* margin-top: 100px;*/
}
.detail a {
  text-decoration: none;
  color: #25383f;
  font-family: "Roboto Condensed";
  font-weight: bold;
  font-size: clamp(0.9rem, 0.7rem + 3.5vw, 1.5725rem);
  border: #25383f solid 5px;
  padding: 10px;
  width: fit-content;
  margin-top: 20px;
}
@media (max-width: 926px) {
  .bottle {
    max-height: 345px;
  }
  .bottle-detail {
    display: flex;
    justify-content: space-evenly;
  }
  .bottle-detail ul {
    padding-left: none;
    margin-top: 40px;
  }
}
@media (max-width: 724px) {
  ul {
    padding-top: 0;
  }
}
@media (max-width: 553px) {
  .bottle-detail {
    flex-direction: column;
  }
  ul {
    padding-left: 0;
    align-items: center;
  }
  .bottle {
    align-self: center;
    margin-top: 10px;
    width: min(191px, 30%);
  }
}
</style>
