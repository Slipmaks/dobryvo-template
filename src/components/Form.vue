<template>
  <div>
    <input
      type="text"
      placeholder="input text"
      v-model="typeOfСrop.inputValue"
      @blur="validate(typeOfСrop)"
    />
    <p v-if="typeOfСrop.error.length">{{ typeOfСrop.error }}</p>
  </div>
  <div>
    <input
      type="text"
      placeholder="input text"
      v-model="yieldValue.inputValue"
      @blur="validate(yieldValue.inputValue)"
    />
    <p v-if="yieldValue.error.length">{{ yieldValue.error }}</p>
  </div>
</template>
<script>
import { reactive, ref } from "vue";

export default {
  setup() {
    const typeOfСrop = reactive({ inputValue: "", error: "" });
    const yieldValue = ref({ inputValue: "", error: "" });
    const stringValidate = new RegExp("[0-9]");

    function validate(val) {
      console.log(val.inputValue);
      if (val.inputValue.match(stringValidate)) {
        val.error.value = "";
      } else if (val.value == 0) {
        val.error.value = "enter the value";
      } else {
        val.error.value = "only number";
      }
      console.log("exit");
    }
    return { validate, typeOfСrop, yieldValue };
  },
};
</script>
