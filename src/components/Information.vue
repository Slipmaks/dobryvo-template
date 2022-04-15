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

  justify-content: space-between;
}
.right-side {
  width: 507px;
  height: 527px;
  background-image: url(../assets/evergeen-souse/Side.png);
}
</style>
