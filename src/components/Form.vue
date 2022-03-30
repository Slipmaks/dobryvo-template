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
    const stringValidate = new RegExp("[^0-9]");

    function validate(objName) {
      console.log(objName.inputValue);
      if (objName.inputValue == 0 || objName.inputValue.match(stringValidate) ||objName.inputValue == undefined) {
        objName.error = "enter the value";
      } else{
        objName.error = ""
      }
     console.log(objName)
    }
    return { validate, typeOfСrop, yieldValue };
  },
};
</script>
