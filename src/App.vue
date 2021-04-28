<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-6 m-auto text-center mt-5 rounded-3">
        <div class="bg-light w-100 h-100 border border-dark">
          <div class="mb-3">
            <label for="inputOne">Input One</label>
            <input
              type="text"
              class="form-control"
              id="inputOne"
              v-model.number="inputOne"
            />
          </div>
          <div class="mb-3">
            <label for="inputTwo">Input two</label>
            <input
              type="text"
              class="form-control"
              id="inputTwo"
              v-model.number="inputTwo"
            />
          </div>
          <div class="mb-3 mt-3">
            <Button text="Add" class="btn-dark" @click="add()" />
            <Button text="Subtract" class="btn-dark" @click="sub()" />
            <Button text="Multiply" class="btn-dark" @click="multi()" />
            <Button text="Divid" class="btn-dark" @click="divid()" />
          </div>
          <div>
            <span>Result = {{ result }}</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Button from "./components/Button";
export default {
  name: "App",
  components: {
    Button,
  },
  data() {
    return {
      inputOne: 0,
      inputTwo: 0,
      result: 0,
    };
  },
  methods: {
    add() {
      this.result = this.inputOne + this.inputTwo;
    },
    sub() {
      this.result = this.inputOne - this.inputTwo;
    },
    multi() {
      this.result = this.inputOne * this.inputTwo;
    },
    divid() {
      this.result = this.inputOne / this.inputTwo;
    },
  },
};
</script>

<style>
html,
body {
  width: 100%;
  height: 100%;
}
</style>
