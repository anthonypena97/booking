<template>
  <div class="text-area">
    <div v-if="label">{{ label }}</div>
    <textarea
      v-model="text"
      :rows="rows"
      :cols="cols"
      @click="sendBack()"
    ></textarea>
  </div>
</template>

<script>
export default {
  name: "TextArea",
  components: {},
  data() {
    return {};
  },
  mounted: {},
  props: {
    text: String,
    label: String,
    rows: Number,
    cols: Number,
  },
  methods: {
    sendBack() {
      this.$emit("change-event", this.text);
    },
  },
};
</script>
<style scoped>
.text-area {
}
</style>
