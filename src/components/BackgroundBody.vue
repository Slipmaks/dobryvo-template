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
@media (max-width: 926px) {
  .main-information {
    display: block;
  }
  .left-side {
    height: 490px;
  }
  .right-side {
    height: 800px;
  }
  .left-side,
  .right-side {
    width: 100%;
  }
}
@media (max-width: 554px) {
  .left-side {
    height: 752px;
  }
  .right-side {
    max-width: 100%;
    height: 100vh;
  }
}
@media (max-width: 456px) {
  .left-side {
    height: 678px;
  }
}
</style>
