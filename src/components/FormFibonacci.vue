<template>
  <form @change="onChange" class="form" action="">
    <input
      class="input input__value"
      type="number"
      placeholder="Input"
      value=""
    />
    <input
      class="input input__result"
      type="text"
      placeholder="Result:XX"
      value=""
      disabled
    />
    <button class="button" type="button">Calculate</button>
  </form>
</template>

<script>
export default {
  methods: {
    onChange() {
      const inputValue = document.querySelector(".input__value").value;
      const result = [0, 1];

      for (let i = 2; i <= inputValue; i++) {
        const prevNum1 = result[i - 1];
        const prevNum2 = result[i - 2];
        result.push(prevNum1 + prevNum2);
      }

      const fibonacciNumber = result.pop();
      document.querySelector(".input__result").value = fibonacciNumber;
    },
  },
};
</script>

<style>
.form {
  display: flex;
  flex-direction: column;
}

.input {
  padding: 1px 15px;
  width: 450px;
  height: 40px;
  background-color: #fff;
  font-size: 20px;
  color: #4a4a4a;
  border: none;
  outline: none;
  border: 1px solid #c2c2c2;
}

.input__value {
  display: block;
  margin-bottom: 15px;
}

.input__result {
  margin-bottom: 90px;
}

.button {
  background-color: #44e320;
  color: #fff;
  border: none;
  border-radius: 5px;
  width: 200px;
  height: 60px;
  font-size: 20px;
  margin-left: auto;
  margin-right: auto;
  cursor: pointer;
  transition: all 0.3s ease;
}

.button:hover {
  opacity: 0.5;
}

.disabled {
  background-color: #4a4a4a;
}
</style>
