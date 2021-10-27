<template>
  <div class="input">
    <input v-model="text" @blur="sendBack()"/>
  </div>
</template>

<script>
export default {
  name: "Input",
  components: {},
  data() {
    return {
        
    };
  },
  props: {
    text: String,
    label: String,
  },
  methods: {
      sendBack() {
          this.$emit("change-event", this.text);
      }
  },
};
</script>

<style scoped>
.input {
  width: 600px;
}
</style>
