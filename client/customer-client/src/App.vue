<template>
  <div id="app">
    <Button text="whatever" label="yo" @click-event="click()" />
    <Input text="input text" label="input" @change-event="change($event)"/>
    <TextArea text="here's some text" label="type in the box" cols="5" rows="5" @change-event="change($event)" />
  </div>
</template>

<script>
import Button from "./components/Button.vue";
import Input from "./components/Input.vue";
import TextArea from "./components/TextArea.vue";


// TODO: stop mutating props directly in child components
// probably need to add a computed property or a 'local version' of the prop
export default {
  name: "App",
  components: {
    Button,
    Input,
    TextArea
  },
  methods: {
    click() {
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
