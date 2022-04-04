<template>
  <div>
    <p>Выберете культуру</p>
    <select v-model="typeOfСrop.inputValue" @blur="validate(typeOfСrop)">
      <option value="3100">Пшеница ≈ 3100 грн / т</option>
      <option value="3300">Гречка ≈ 3300 грн / т</option>
      <option value="2900">Картофель ≈ 2900 грн / т</option>
    </select>
    <p v-if="typeOfСrop.error.length">{{ typeOfСrop.error }}</p>
  </div>
  <div>
    <p>Урожайность, ц/га</p>
    <input
      type="text"
      placeholder="20"
      v-model="yieldValue.inputValue"
      @blur="validate(yieldValue)"
    />
    <p v-if="yieldValue.error.length">{{ yieldValue.error }}</p>
  </div>
  <div>
    <p>Стоимость хим. удобрениея, грн/га</p>
    <input
      type="text"
      placeholder="3000"
      v-model="fertilizerPrice.inputValue"
      @blur="validate(fertilizerPrice)"
    />
    <p v-if="fertilizerPrice.error.length">{{ fertilizerPrice.error }}</p>
  </div>
  <div>
    <p>Посевная площадь, га</p>
    <input
      type="text"
      placeholder="10"
      v-model="sownArea.inputValue"
      @blur="validate(sownArea)"
    />
    <p v-if="sownArea.error.length">{{ sownArea.error }}</p>
  </div>
</template>
<script>
import { ref } from "vue";

export default {
  setup() {
    const typeOfСrop = ref({ inputValue: "", error: "" });
    const yieldValue = ref({ inputValue: "", error: "" });
    const fertilizerPrice = ref({ inputValue: "", error: "" });
    const sownArea = ref({ inputValue: "", error: "" });
    const stringValidate = new RegExp("[^0-9]");

    function validate(objName) {
      if (
        objName.inputValue == 0 ||
        objName.inputValue.match(stringValidate) ||
        objName.inputValue == undefined
      ) {
        objName.error = "enter correct the value";
      } else {
        objName.error = "";
      }
    }
    return { validate, typeOfСrop, yieldValue, fertilizerPrice, sownArea };
  },
};
</script>
