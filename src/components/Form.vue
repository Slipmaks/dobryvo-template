<template>
  <div class="main">
    <div class="form">
      <h1>ПОСЧИТАТЬ ПРИБЫЛЬ</h1>
      <p>ДОБРИВО ЭФФЕКТИВНЕЕ ХИМИИ</p>
      <hr />
      <div>
        <p>Выберете культуру</p>
        <select v-model="typeOfСrop.inputValue" @blur="validate(typeOfСrop)">
          <option value="3100">Пшеница ≈ 3100 грн / т</option>
          <option value="3300">Гречка ≈ 3300 грн / т</option>
          <option value="2900">Картофель ≈ 2900 грн / т</option>
        </select>
        <p class="error" v-if="typeOfСrop.error.length">
          {{ typeOfСrop.error }}
        </p>
      </div>
      <div>
        <p>Урожайность, ц/га</p>
        <input
          type="text"
          placeholder="20"
          v-model="yieldValue.inputValue"
          @blur="validate(yieldValue)"
        />
        <p class="error" v-if="yieldValue.error.length">
          {{ yieldValue.error }}
        </p>
      </div>
      <div>
        <p>Стоимость хим. удобрениея, грн/га</p>
        <input
          type="text"
          placeholder="3000"
          v-model="fertilizerPrice.inputValue"
          @blur="validate(fertilizerPrice)"
        />
        <p class="error" v-if="fertilizerPrice.error.length">
          {{ fertilizerPrice.error }}
        </p>
      </div>
      <div>
        <p>Посевная площадь, га</p>
        <input
          type="text"
          placeholder="10"
          v-model="sownArea.inputValue"
          @blur="validate(sownArea)"
        />
        <p class="error" v-if="sownArea.error.length">
          {{ sownArea.error }}
        </p>
      </div>
      <hr />
      <p>ПРИБЫЛЬ ОТ ДОБРИВА</p>
      <h1>{{ profitVal }}</h1>
      <p>грн</p>
    </div>
  </div>
</template>
<script>
import { ref } from "vue";

export default {
  setup() {
    const typeOfСrop = ref({ inputValue: "", error: false });
    const yieldValue = ref({ inputValue: "", error: false });
    const fertilizerPrice = ref({ inputValue: "", error: false });
    const sownArea = ref({ inputValue: "", error: false });
    const stringValidate = new RegExp("[^0-9]");
    const profitVal = ref(0);

    function validate(objName) {
      if (objName.inputValue == 0 || objName.inputValue == undefined) {
        objName.error = "Введите значение";
      } else if (objName.inputValue.match(stringValidate)) {
        objName.error = "Только цифры";
      } else {
        objName.error = false;
        calcPrifit();
      }
    }
    function calcPrifit() {
      if (
        fertilizerPrice.value.inputValue &&
        typeOfСrop.value.inputValue &&
        yieldValue.value.inputValue &&
        sownArea.value.inputValue
      ) {
        profitVal.value =
          +typeOfСrop.value.inputValue * +yieldValue.value.inputValue -
          +fertilizerPrice.value.inputValue *
            (+yieldValue.value.inputValue / +sownArea.value.inputValue);
        profitVal.value = profitVal.value.toFixed(1);
      } else {
        profitVal.value = 0;
      }
    }

    return {
      validate,
      typeOfСrop,
      yieldValue,
      fertilizerPrice,
      sownArea,
      profitVal,
    };
  },
};
</script>
<style>
.error {
  color: brown;
  position: absolute;
  padding-left: 6%;
}
.main {
  width: 320px;
  height: 594px;
  background-color: #e9e5e4;
  display: flex;
  flex-direction: column;
}
.form {
  border: 2px dashed #a7a9ac;
  display: flex;
  flex-direction: column;
  text-align: center;
  justify-content: space-evenly;
  margin: 13px;
  height: 100%;
  background-color: #f2f0ef;
}
@media (max-width: 926px) {
  .main {
    margin-top: 50px;
    margin-bottom: 50px;
  }
}
@media (max-width: 526px) {
  .main {
    margin-top: 100px;
  }
}
</style>
