<template>
  <div class="main-information">
    <div class="left-side"></div>
    <div class="right-side"></div>
  </div>
</template>
<script></script>
<style>
.main-information {
  display: flex;
}
.left-side,
.right-side {
  height: 526px;
}
.left-side {
  width: 60%;
}
.right-side {
  width: 40%;
  background-image: url(../assets/evergeen-souse/Side.png);
  background-size: cover;
  background-repeat: no-repeat;
}
@media (max-width: 767px) {
  .main-information {
    display: block;
  }
  .left-side,
  .right-side {
    width: 100%;
  }
}
</style>
