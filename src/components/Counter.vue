<template>
  <div>
    <h1>Vuex Counter</h1>
    <div class="counter">0</div>
    <button class="sign">-</button>
    <input class="input" type="number" v-model="value" />
    <button class="sign">+</button>
  </div>
</template>

<script>
export default {
  name: "Counter",
  data() {
    return {
      counter: 0,
      value: 1,
    };
  },
};
</script>

<style scoped>
.counter {
  font-size: 5rem;
}

.sign {
  border-radius: 100%;
  border: none;
  width: 2rem;
  height: 2rem;
  font-weight: 700;
  cursor: pointer;
}

.input {
  padding: 0.4rem;
  margin: 0 0.5rem;
  text-align: center;
}
</style>
