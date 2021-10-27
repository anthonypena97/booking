<template>
  <div class="btn">
      <div v-if="label"> {{ label }} </div>
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
      text: String,
      label: String
  },
  methods: {
      sendBack() {
          this.$emit("click-event");
          // creates a new type of DOM event called "something"
      }
  }
}
</script>

<style scoped>
.btn {
  width: 600px;
}

</style>
