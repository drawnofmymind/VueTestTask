<template>
  <div>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "RadioGroup",
  model: {
    prop: "value",
    event: "input",
  },
  props: {
    value: {
      type: [String, Number],
    },
    disabled: {
      type: Boolean,
      default: false,
    },
  },
  provide() {
    return {
      radioGroup: this,
    };
  },
  methods: {
    handleChange(newValue) {
      if (!this.disabled) {
        this.$emit("input", newValue);
      }
    },
  },
};
</script>
