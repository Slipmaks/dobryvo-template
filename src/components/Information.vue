<template>
  <div class="main-information">
    <div class="left-side">
      <h1>ОРГАНИЧЕСКОЕ НАНО-УДОБРЕНИЕ ДОБРИВО</h1>
    </div>
    <div class="right-side">
      <Form />
    </div>
  </div>
</template>
<script>
import Form from "./Form.vue";
export default {
  components: {
    Form,
  },
};
</script>
<style>
.main-information {
  display: flex;
}
.left-side {
  width: 50%;
}
.right-side {
  height: 526px;
  width: 50%;
  background-image: url(../assets/evergeen-souse/Side.png);
  background-size: cover;
  background-repeat: no-repeat;
}
.information-wrapper {
  width: 1000px;
  max-width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
