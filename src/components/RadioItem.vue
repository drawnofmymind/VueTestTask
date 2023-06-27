<template>
  <div>
    <input
      type="radio"
      :value="value"
      :checked="value === radioGroup.value"
      :disabled="radioGroup.disabled || disabled"
      @change="handleChange"
    />
    <label>{{ label }}</label>
  </div>
</template>

<script>
export default {
  name: "RadioItem",
  inject: ["radioGroup"],
  props: {
    value: {
      type: [String, Number],
      required: true,
    },
    label: {
      type: String,
      required: true,
    },
    disabled: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    // eslint-disable-next-line no-unused-vars
    handleChange(event) {
      if (!this.disabled) {
        this.$emit("change", this.value);
        this.radioGroup.handleChange(this.value);
      }
    },
  },
};
</script>
