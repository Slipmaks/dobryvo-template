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
      @blur="validate(yieldValue)"
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

    function validate(name) {
      console.log(name)
      console.log(name.inputValue);
      if (name.inputValue == 0 || name.inputValue === undefined) {
        name.error = "enter the value";
      } else if (name.inputValue.match(stringValidate)) {
        name.error = "";
      } else {
        name.error = "only number";
      }
      console.log("exit");
    }
    return { validate, typeOfСrop, yieldValue };
  },
};
</script>
