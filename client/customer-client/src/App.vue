<template>
  <div id="app">
    <Button text="whatever" label="yo" @click-event="method()" />
    <Input text="input text" label="input" @change-event="change($event)"/>
  </div>
</template>

<script>
import Button from "./components/Button.vue";
import Input from "./components/Input.vue";

export default {
  name: "App",
  components: {
    Button,
    Input
  },
  methods: {
    method() {
      console.log("button clicked");
    },
    change(val) {
      console.log(val);
    }
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
