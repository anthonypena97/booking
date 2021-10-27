<template>
  <div id="btn">
      <button @click="sendBack()">{{ text }}</button>
  </div>
</template>

<script>

export default {
  name: 'Button',
  components: {
  },
  data() {
    return {
    }
  },
  props: {
      text: String
  },
  methods: {
      sendBack() {
          this.$emit("something");
      }
  }
}
</script>

<style scoped>
#btn {
  width: 6000px;
}
</style>
