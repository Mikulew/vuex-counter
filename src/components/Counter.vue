<template>
  <div>
    <h1>Vuex Counter</h1>
    <div class="counter">{{ counter }}</div>
    <button class="sign" @click="substractFromCounter(parseInt(value))">
      -
    </button>
    <input class="input" type="number" v-model="value" />
    <button class="sign" @click="addToCounter(parseInt(value))">+</button>
    <div>
      <button class="button" @click="addRandomNumber">Add Random Number</button>
    </div>
  </div>
</template>

<script>
import { mapState, mapMutations, mapActions } from "vuex";

export default {
  name: "Counter",
  data() {
    return {
      value: 1,
    };
  },
  computed: {
    ...mapState(["counter"]),
  },
  methods: {
    ...mapMutations(["addToCounter", "substractFromCounter"]),
    ...mapActions(["addRandomNumber"]),
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

.button {
  border-radius: 0.5rem;
  border: none;
  width: auto;
  background-color: #41b983;
  margin-top: 1rem;
  padding: 0.5rem;
  color: #ffffff;
  cursor: pointer;
}
</style>
